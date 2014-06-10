---
layout: post
title: agf-mad - Ajout de la méthode convertRowIndexToModel sur la RequestTable
tags: [framework-1-74,codjo-mad]
---
La méthode suivante a été ajoutée à la ```RequestTable```
```
    public int convertRowIndexToModel(int viewRowIndex)
```

Cette méthode permet de convertir un indice de vue en un indice de modèle.

A partir d'un indice de la vue (par exemple, dans un ```TableCellRenderer```),  il est donc possible de récupérer des données du ```DataSource``` de la ```RequestTable``` en se basant sur l'indice du modèle retournée par cette méthode.