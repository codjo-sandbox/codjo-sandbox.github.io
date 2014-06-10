---
layout: post
title: agf-mad - New action SpreadsheetExportAction
tags: [codjo-mad,framework-1-143]
---
<u>Context</u>:

Existing export action ```ExportAction``` and ```ExportAllPagesAction``` generated text files which were automatically converted in Excel, e.g. value ```01``` would appear as ```1```.

Furthermore, content of the generated file was exactly the same as the ```RequestTable``` from which the export was launched.


<u>Description</u>:

The new ```SpreadsheetExportAction``` has been created and generate a binary spreadsheet for Excel. Thus, values are unaltered when exported.

Furthermore, it is easier to extend this action to change the content of the generated spreadsheet :

```protected String[[]] getHeaders();

protected Iterator<Row> getRowIterator();
```
<u>Example</u>:

```...
AbstractGuiAction action = new SpreadsheetExportAction(guiContext, requestTable);
toolBar.replace(RequestToolBar.ACTION_EXPORT_ALL_PAGES, action);
...
```
{info:title=RequestToolBar}The default export action for the ```RequestToolBar``` still remains ```ExportAllPagesAction```.{info}


See : [[codjo-mad - Utilisation|agf-mad - Utilisation#excelExportAnchor]]