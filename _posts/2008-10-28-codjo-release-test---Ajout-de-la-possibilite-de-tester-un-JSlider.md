---
layout: post
title: agf-release-test - Ajout de la possibilité de tester un JSlider
tags: [framework-1-68,codjo-release-test]
---
Pour pouvoir tester les composants JSlider, la balise <assertValue> a été enrichie (classe AssertValueStep).

Exemple d'utilisation:

Pour tester un composant JSlider défini de la manière suivante:
```
JSlider slider = new JSlider() ;
slider.setMinimum(1) ;
slider.setMaximum(10) ;
slider.setValue(5);
```
Pour tester que la valeur du composant est bien 5, il faut saisir dans le test:
```
<assertValue name="slider" expected="5"/>
```