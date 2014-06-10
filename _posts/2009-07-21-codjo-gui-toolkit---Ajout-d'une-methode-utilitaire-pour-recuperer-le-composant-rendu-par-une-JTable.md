---
layout: post
title: agf-gui-toolkit - Ajout d'une méthode utilitaire pour récupérer le composant rendu par une JTable
tags: [framework-1-105,codjo-gui-toolkit]
---
Une méthode utilitaire ```getRenderedComponentAt``` a été ajoutée dans ```TableUtil```. Elle permet de récupérer facilement le composant rendu par une ```JTable``` dans une cellule donnée.

<u>API</u> :
```
public static Component getRenderedComponentAt(JTable table, int rowIndex, int columnIndex)
```