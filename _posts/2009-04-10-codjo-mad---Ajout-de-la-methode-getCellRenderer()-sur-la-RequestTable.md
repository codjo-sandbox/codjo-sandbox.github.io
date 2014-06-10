---
layout: post
title: agf-mad - Ajout de la méthode getCellRenderer() sur la RequestTable
tags: [codjo-mad,framework-1-91]
---
La méthode suivante à été ajoutée sur la ```RequestTable``` :
``` public TableCellRenderer getCellRenderer(final String fieldName)```

Elle retourne le renderer associé à une colonne correspondant à un nom de champ défini sur la ```Preference```.
