---
layout: post
title: agf-mad - Ajout d'une méthode pour calculer la meilleure dimension de la liste de choix en fonction de son contenu
tags: [framework-1-113,codjo-mad]
---
La méthode ```Dimension getPreferredSizeForContent()``` permet d'obtenir les dimensions les plus adéquates pour la ```RequestComboBox``` en fonction de son contenu. Ainsi, l'utilisateur peut spécifier la taille préférée pour la liste de choix au lieu de laisser le layout le faire :

```
RequestComboBox comboBox = new RequestComboBox();
[[...]]
comboBox.load();
comboBox.setPreferredSize(comboBox.getPreferredSizeForContent());
```

Les dimensions renvoyées correspondront en longueur à l'élément le plus long de la liste de choix, et en hauteur à la hauteur d'une ligne de texte.

Si la liste de choix est vide, alors une taille minimum est renvoyée.