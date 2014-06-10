---
layout: post
title: agf-release-test - Expected column count added on AssertTableExcel step
tags: [framework-1-131,codjo-release-test,hot-topics]
---
<u>Context</u>:
An ```AssertTableExcel``` step didn't fail despite the fact that the table&nbsp;had more columns than&nbsp;the Excel benchmark.&nbsp;

<u>Description</u>:
The ```AssertTableExcel``` step was extended to be able to specify the expected number of table columns.

<u>Example</u>:

In the following sample, we want to make sure that the table is 5 column-wide

```<assertTableExcel name="PorfolioCode"
                  file="myTable.xls"
                  sheetName="portfolio_sheet"
                  expectedRowCount="12"
                  expectedColumnCount="5" />
```

see: [[codjo-release-test |agf-release-test - Tags IHM#assertTableExcel]]