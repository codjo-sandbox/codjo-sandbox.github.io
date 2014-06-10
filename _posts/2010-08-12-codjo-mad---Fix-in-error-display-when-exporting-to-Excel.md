---
layout: post
title: agf-mad - Fix in error display when exporting to Excel
tags: [framework-1-160,codjo-mad]
---
<u>Context:</u>
When exporting data from GUI to Excel, if the export does not succeed in opening the Excel file, the name of the file was supposed to be displayed in an error dialog. But, in fact, a "null" name was displayed (see following screenshot).
![Alt attribute text Here](attachments/Erreur export Excel Before.JPG|thumbnail)

<u>Description:</u>
The bug has been fixed in the ```ExportUtil``` class (see following screenshot).
![Alt attribute text Here](attachments/Erreur export Excel After.JPG|thumbnail)

See [[framework:/2010/06/14/codjo-mad - Change Export Excel on RequestToolBar] and [framework:/2010/04/19/agf-mad - New action SpreadsheetExportAction]]