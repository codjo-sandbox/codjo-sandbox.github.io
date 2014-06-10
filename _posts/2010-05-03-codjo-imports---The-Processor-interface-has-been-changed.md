---
layout: post
title: agf-imports - The Processor interface has been changed
tags: [framework-1-145,codjo-imports]
---
<u>Context</u>:

The ```preProceed``` method of the ```Processor``` interface need to be changed to be like the ```postProceed``` method.

<u>Description</u>:

The interface is now :

```
public interface Processor {
    void preProceed(Connection con, String quarantineTableName, File file) throws SQLException;


    void postProceed(Connection con, String quarantineTableName, File file, ImportFailureException ex)
          throws SQLException;
}
```