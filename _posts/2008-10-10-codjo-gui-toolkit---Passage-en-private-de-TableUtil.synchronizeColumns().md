---
layout: post
title: agf-gui-toolkit - Passage en private de TableUtil.synchronizeColumns()
tags: [framework-1-65,codjo-gui-toolkit]
---
La méthode suivante est passée privée :
```
private static void synchronizeColumns(final JTable masterTable, final JTable... slaveTables)
```

Il faut utiliser cette méthode à la place :
```
public static void synchronizeTableColumns(final JTable... tables)
```
\\

Par exemple, il faut remplacer :
```
TableUtil.synchronizeColumns(table1, table2, table3);
```
par :
```
TableUtil.synchronizeTableColumns(table1, table2, table3);
```