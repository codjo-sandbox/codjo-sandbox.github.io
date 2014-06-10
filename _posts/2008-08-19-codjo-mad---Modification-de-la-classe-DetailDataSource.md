---
layout: post
title: agf-mad - Modification de la classe DetailDataSource
tags: [framework-1-57,codjo-mad]
---
Modification de la méthode ```getFieldValue``` en remplaçant le code suivant
```
return getSelectedRow().getFieldValue(fieldName)
```
par le code suivant :
```
Row selectedRow = getSelectedRow();
if (selectedRow != null && selectedRow.getFieldCount() > 0) {
    return selectedRow.getFieldValue(fieldName);
} else {
    return null;
}
```
&nbsp;Ceci permet de retourner ```null``` au lieu d'une ```NullPointerException```