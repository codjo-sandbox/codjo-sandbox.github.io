---
layout: post
title: agf-mad - Selection of row to save in DetailDataSource
tags: [codjo-mad,framework-1-119]
---
The ```DetailDataSource``` could only save the first loaded row, even if the initial load request returned several rows.

You can now set a current row by calling the ```setSelectedRow()``` method. The load and save functions will apply to this row.&nbsp;

Example of code usage :
```
detailDataSource.setSelectedRowIndex(selectedRowIndex);
detailDataSource.updateGuiFields(); // Refresh the UI with the current row data
// Some bound text fields were changed
detailDataSource.save(); // The current row will be saved
```