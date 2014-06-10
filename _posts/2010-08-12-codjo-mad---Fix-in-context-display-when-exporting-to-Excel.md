---
layout: post
title: agf-mad - Fix in context display when exporting to Excel
tags: [framework-1-160,codjo-mad]
---
<u>Context:</u>
When exporting data from GUI to Excel, the name of the Excel file was supposed to be displayed in the context bar. But, in fact, a "null" name was displayed (see following screenshot).
![Alt attribute text Here](attachments/Export Excel Before.JPG|thumbnail)

<u>Description:</u>
The bug has been fixed in the ```ExportExcelBuilder``` class (see following screenshot).
![Alt attribute text Here](attachments/Export Excel After.JPG|thumbnail)

See [[framework:/2010/06/14/codjo-mad - Change Export Excel on RequestToolBar] and [framework:/2010/04/19/agf-mad - New action SpreadsheetExportAction]]