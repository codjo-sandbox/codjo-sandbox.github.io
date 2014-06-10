---
layout: post
title: agf-gui-toolkit - Synchronisation de la sélection de plusieurs JTables
tags: [codjo-gui-toolkit,framework-1-83]
---
Une méthode utilitaire a été ajoutée à ```TableUtil```. Elle permet de synchroniser la sélection et le mode de sélection de plusieurs ```JTable```.

```
        TableUtil.synchronizeTableSelection(ListSelectionModel.SINGLE_SELECTION,
                   table1, table2, table3);
```