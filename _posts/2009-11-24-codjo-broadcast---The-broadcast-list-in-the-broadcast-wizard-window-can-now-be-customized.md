---
layout: post
title: agf-broadcast - The broadcast list in the broadcast wizard window can now be customized
tags: [framework-1-123,codjo-broadcast,hot-topics]
---
<u>Context</u>

The broadcast list in the broadcast wizard window could not be customized.

<u>Description</u>

It is now possible to set the handler used to display the broadcast list in the broadcast wizard window.

Like the default handler ```selectAllBroadcastFiles``` from codjo-broadcast, the handler must return at least the attributes ```fileId``` and ```fileName``` (it's the ```fileName``` attribute that is displayed in the combobox)

```
// in your MyApplicationGuiPlugin
broadcastGuiPlugin.getConfiguration().setWizardBroadcastSelector(
                         new MyBroadcastSelector(madConnectionPlugin.getOperations()));
```

```
   public class MyBroadcastSelector implements BroadcastSelector {
      private MadConnectionOperations madConnectionOperations;

   public CreoBroadcastSelector(MadConnectionOperations madConnectionOperations) {
      this.madConnectionOperations = madConnectionOperations;

   public Result selectBroadcastItems(String[[]] columns) throws RequestException {
      SelectRequest select = new SelectRequest();
      FieldsList list = new FieldsList();
      list.addField("someData", "dummy");
      select.setId("mySelectBroadcast");
      select.setAttributes(columns);
      select.setSelector(list);
      return madConnectionOperations.sendRequest(select);
   }
}
```

```
/** Handler sample **/
<handler-sql id="mySelectBroadcast">
   <attributes>
      <name>fileId</name>
      <name>fileName</name>
   </attributes>
   <query>
      <![CDATA[
	select
	  PM_BROADCAST_FILES.FILE_ID,
	  PM_BROADCAST_FILES.FILE_NAME
	from PM_BROADCAST_FILES
        inner join PM_MY_BROADCAST_CONFIG
        on PM_BROADCAST_FILES.FILE_ID = PM_MY_BROADCAST_CONFIG.FILE_ID
        and ...
        where PM_MY_BROADCAST_CONFIG.SOME_DATA = ? and ...
	]]>
   </query>
   <arg type="string">someData</arg>
</handler-sql>
```

Note : The ```BroadcastGuiPlugin``` constructor has changed. It takes now a ```MadConnectionPlugin``` argument. Through dependency injection, there was no impact on your code.