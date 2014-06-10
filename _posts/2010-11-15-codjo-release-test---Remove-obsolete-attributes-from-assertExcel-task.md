---
layout: post
title: agf-release-test - Remove obsolete attributes from assertExcel task
tags: [framework-1-174,codjo-release-test]
---
<u>Context</u>:
Due to the last modification of excel file comparison (See [[here|framework:/2010/10/22/codjo-release-test - Add cell style assertions in the assert-excel step]]), ```columnCount``` and ```rowCount``` are no longer used.

<u>Description</u>:
We removed them from the ```assertExcel``` task.

<u>Example</u>:

* Before:
```xml
<assert-excel expected="ExportXL_etalon.xls" columnCount="10" rowCount="10"/>
```

* Now:
```xml
<assert-excel expected="ExportXL_etalon.xls"/>
```