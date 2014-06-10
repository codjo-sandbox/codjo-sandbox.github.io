---
layout: post
title: agf-release-test - Correction sur AssertTableStep
tags: [framework-1-107,codjo-release-test]
---
Prenons l'exemple suivant :
```xml
<assertTable name="SecuritiesTable" column="ISIN" row="0" expected="5968"/>
```

Dans le cas où la valeur réelle était nulle, la méthode ```getActualValue(...)``` générait une ```NullPointerException``` lors de l'appel de ```toString()```.
```
private String getActualValue(JTable table, int realColumn, TableCellRenderer renderer) {
   ...
   return actualValue.toString();
}
```

A présent, la méthode utilise ```String.valueOf(...)``` pour retourner la valeur réelle :
```
private String getActualValue(JTable table, int realColumn, TableCellRenderer renderer) {
   ...
   return String.valueOf(actualValue);
}
```