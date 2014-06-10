---
layout: post
title: agf-mad - Auto-commit functionality added to RequestTable
tags: [framework-1-149,codjo-mad,hot-topics]
---
<u>Context</u>
Sometimes an editable table is not supposed to have a validation button to save its modifications.

<u>Description</u>
A method ```setAutoCommit(boolean autocommit, String... requiredFields)``` has been added to the ```RequestTable```.

The ```requiredFields``` argument to the ```setAutoCommit``` method is a list (optional) of fields which **must have not null values** for the save to be effectively triggered. This list will usually be the primary key fieldnames, or a special hidden value of the ```RequestTable``` that will allow finer control over when a save is called.

<u>Examples</u>
To activate auto-commit, follow the example below:
```
requestTable.setAutoCommit(true, "field1", "field2", "field3");
```
Any update or delete to the table's data source will trigger a save from that moment.

Auto-commit can be disabled as follows:
```
requestTable.setAutoCommit(false);
```

See [[codjo-mad]]