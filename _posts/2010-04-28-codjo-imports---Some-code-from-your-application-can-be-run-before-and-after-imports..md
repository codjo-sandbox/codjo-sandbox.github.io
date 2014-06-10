---
layout: post
title: agf-imports - Some code from your application can be run before and after imports.
tags: [framework-1-144,codjo-imports]
---
<u>Context</u>
For ORBIS migration we need to run code just after imports and rename the imported files.


<u>Description</u>
We have done a code refactoring on the existing Processor (which allowed us to only run code before import) to also add the ability to run code just after import.

In your plugin ```applicationServerPlugin``` :
```
ImportServerPluginConfiguration importServerPluginConfig = importServerPlugin.getConfiguration();

importServerPluginConfig.setProcessorFor("IDEE", new MyIdeeProcessor()); // ("IDEE" is a source system)
importServerPluginConfig.setProcessorFor("VLODDO", new DeleteQuarantineProcessor());
```

You must override either the ```preProceed``` or ```postProceed``` methods (or both if needed) of the ```ProcessorAdapter``` class (or simply implement the ```Processor``` interface) to run code before or/and after imports.

In the ```postProceed``` method, the ```ImportFailureException``` exception parameter can be tested against ```null``` to know if the import has failed.

```
public class DeleteQuarantineProcessor extends ProcessorAdapter {

    @Override
    public void preProceed(Connection con, String tableName) throws SQLException {
        Statement stmt = con.createStatement();
        stmt.executeUpdate("delete from " + tableName);
    }    
}
```

```
class MyIdeeProcessor implements Processor {

    @Override
    public void preProceed(Connection con, String tableName) throws SQLException {
        Statement stmt = con.createStatement();
        stmt.executeUpdate("delete from " <u> tableName </u> " where ERROR_TYPE > 0" );
    }

    @Override
    public void postProceed(Connection con, String tableName, File file, ImportFailureException ex) {
        Date date = new GregorianCalendar().getTime();
        SimpleDateFormat simpleDateFormat = new SimpleDateFormat("_yyyyMMdd_HHmmss");
	...
	...
        String fileName = file.getName() + simpleDateFormat.format(date);
	if (ex != null) {
            file.renameTo(new File(file.getParent(), fileName + "_KO"));
	}
	 else {
	    file.renameTo(new File(file.getParent(), fileName + "_OK"));
	}
    }
}
```

