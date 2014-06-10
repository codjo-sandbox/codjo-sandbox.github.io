---
layout: post
title: agf-gui-toolkit - Ajout d'un JPanel sans remplissage vertical sur LabelledItemPanel
tags: [framework-1-82,codjo-gui-toolkit]
---
Nouvelle méthode ```addItem(String labelText, JPanel panel, boolean fillVertical)```:
- String labelText : libellé à afficher à côté du composant
- JPanel panel : composant a afficher (toujours un JPanel contenant plusieurs Component)
- boolean fillVertical : si ```vrai``` alors le composant prend tout l'espace vertical disponible dans le ```LabelledItemPanel``` ; si ```faux``` alors le composant prend uniquement la taille verticale qui lui est nécessaire.