---
layout: post
title: agf-mad - Excel cell formats now properly set in export action
tags: [codjo-mad,framework-1-161,hot-topics]
---
<u>Context</u>
When exporting a table's content to Microsoft Excel, all the cells of the new spreadsheet were in the **Default** format, and cells with numeric content displayed a warning sign in the upper left-hand corner, like the one depicted below.

![Alt attribute text Here](attachments/exportexcelavant.PNG)

One would have to select the appropriate values in the spreadsheet and select the "Convert to number" action in the popup menu in order for Excel to apply the appropriate formating where needed.

<u>Description</u>
Now the export action takes into account the ```sorter``` attribute defined in the ```preference.xml``` file.

See : [[codjo-mad - Utilisation|agf-mad - Utilisation#excelExportAnchor]]