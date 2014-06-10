---
layout: post
title: agf-gui-toolkit - Simplification de l'utilisation de la perte globale du focus d'un composant DateField
tags: [framework-1-109,codjo-gui-toolkit]
---
L'ajout d'un FocusListener au composant DateField se fait maintenant de la manière suivante:
```
DateField datefield = new DateField();
dateField.addFocusListener(new MyFocusListener());
```