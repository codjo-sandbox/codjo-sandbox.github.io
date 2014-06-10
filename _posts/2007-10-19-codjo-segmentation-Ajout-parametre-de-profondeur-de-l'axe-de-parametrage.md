---
layout: post
title: agf-segmentation Ajout paramètre de profondeur de l'axe de paramétrage
tags: [framework-1-17,codjo-segmentation]
---
Il est désormais possible de spécifier dans une application la profondeur maximale pour l'arbre de paramétrage des axes de segmentation.

&nbsp;Pour ce faire il suffit de spécifier le paramètre au plugin de segmentation en utilisant la fonction suivante lors de la configuration du plugin dans l'application concernée :
```
// pour une profondeur maximale de 4 par ex :
segmentationGuiPlugin.getConfiguration().setMaximumNodeDepth(4);
```
&nbsp;Par défaut la profondeur maximale de l'arbre est de 98 noeuds + 1 feuille.
\\
\\
\\