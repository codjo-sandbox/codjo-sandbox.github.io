---
layout: post
title: agf-gui-toolkit - Ajout de la possibilité de customiser les composants de sélection des fichiers
tags: [codjo-gui-toolkit,framework-1-47]
---
Il est maintenant possible d'indiquer au ```FileChooserManager``` et au ```FilePathField``` si on veut afficher ou pas les accessoires (recherche, prévisualisation et favoris) dans la boite de dialogue de sélection des fichiers.

Pour cela, il suffit d'appeler la méthode :
```
public void setWithAccessories(boolean withAccessories);
```
La valeur par défaut est ```true```