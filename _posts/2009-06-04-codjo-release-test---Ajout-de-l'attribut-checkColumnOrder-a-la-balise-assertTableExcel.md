---
layout: post
title: agf-release-test - Ajout de l'attribut checkColumnOrder à la balise assertTableExcel
tags: [hot-topics,framework-1-99,codjo-release-test]
---
La balise ```assertTableExcel``` ne testait pas l'ordre des colonnes. C'est maintenant possible grâce au tout nouvel attribut ```checkColumnOrder```.

<u>Exemple</u>
```
<assertTableExcel name="tableWithCellSelectable"
                  file="AssertTableExcel.xls"
                  sheetName="sheet1"
                  checkColumnOrder="true"
                  expectedRowCount="3"/>
```