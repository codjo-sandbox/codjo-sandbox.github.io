---
layout: post
title: agf-test - Upgrade of class ExcelUtil
tags: [framework-1-172,codjo-test,hot-topics]
---
<u>Context</u>
Due to the latest modifications in the framework (See [[codjo-release-test|framework:2010/10/22/agf-release-test - Add cell style assertions in the assert-excel step] and [agf-pom|framework:2010/10/22/agf-pom - New Library jxls available]]) in the ```agf-mad library```, we need to create a unit test that focuses on comparing the result of the ```ExcelExportBuilder``` with an excel file. Moreover, we need to improve the readability of the error message when the test fails.

<u>Description</u>
We move class ```ExcelComparator``` from ```codjo-release-test``` to ```agf-test``` along with other utility classes. 
Now the class ```ExcelUtil``` provides two new methods :
```java
boolean compare(File expectedFile, File actualFile,
                                  String sheetNamesToCompare, String sheetMatchersToApply)

boolean compare(HSSFWorkbook expectedWorkbook, HSSFWorkbook actualWorkbook,
                                  String sheetNamesToCompare, String sheetMatchersToApply)
```
When ```sheetNamesToCompare``` parameter is not set then all sheets will be tested.
When ```sheetMatchersToApply``` parameter is not set then only Content matching will be run.

When the comparison fails, the error message is displayed like the file comparison does :
```
C:\Dev\Temp\ExportSyntheseChantier.xml:44: Couleur de fond des cellules de la feuille 'Feuil1' en erreur.
Excel line 26
	Expected > TRANSPARENT | TRANSPARENT | TRANSPARENT | TRANSPARENT | TRANSPARENT | TRANSPARENT | LIGHT_GREEN |
	Actual   > TRANSPARENT | TRANSPARENT | LIGHT_GREEN | TRANSPARENT | TRANSPARENT | TRANSPARENT | LIGHT_GREEN |
	Gap      > ____________________________*
```

<u>Example</u>:
```java
ExcelUtil.compare(new File("expected_ok.xls"),
                  new File("actual.xls"),
                  "Sheet0,Sheet2",
                  "bold,italic,margin")
```
