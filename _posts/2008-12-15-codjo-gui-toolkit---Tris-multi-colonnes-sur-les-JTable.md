---
layout: post
title: agf-gui-toolkit - Tris multi colonnes sur les JTable
tags: [framework-1-76,codjo-gui-toolkit]
---
La classe ```TableRendererSorter``` a été modifiée afin de pouvoir trier les données d'une JTable en fonction de plusieurs colonnes.
Pour pouvoir trier une table suivant la colonne A (en admettant qu'il y ait des données en doublons) puis suivant la colonne B, il faut double-cliquer sur l'entête de la colonne A puis appuyer sur la touche **ctrl** tout en double-cliquant sur l'entête de B.

La classe ```TableRendererSorter``` devrait être renommée ```TableSorter``` puisqu'elle n'implémente plus l'interface ```TableCellRenderer```. La partie assurant le renderer a été extraite dans la classe ```TableSorterRenderer```.
Idem pour la classe ```TableRendererSorterWithButton```.
