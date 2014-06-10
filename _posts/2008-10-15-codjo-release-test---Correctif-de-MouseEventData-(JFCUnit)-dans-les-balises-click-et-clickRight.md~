---
layout: post
title: agf-release-test - Correctif de MouseEventData (JFCUnit) dans les balises click et clickRight
tags: [framework-1-66,codjo-release-test]
---
La classe ```MouseEventData``` de la librairie JFCUnit (ver 2.0.6) provoquait un bug lors d'un step ```click``` ou ```clickRight``` si le composant en question était un bouton dans un ```JScrollPane```.

Les classes d'implémentations des balises ```click``` et ```clickRight``` héritent de ```com.agf.test.release.task.gui.AbstractClickStep```. Celle-ci utilisait un objet ```MouseEventData``` pour provoquer un déplacement de souris, puis un clic aux coordonnées de l'écran où était censé se trouver le composant concerné. Ces coordonnées étaient calculées par rapport aux coordonnées relatives du composant pour aboutir à des coordonnées absolues à l'écran. Ce calcul était erroné dans le cas d'un composant contenu dans un ```JScrollPane```.

Le correctif est apporté sous la forme d'une classe héritant de ```MouseEventData``` : ```com.agf.test.release.task.gui.ClickMouseEventData```. Cette classe surcharge la méthode incriminée de ```MouseEventData``` et l'empêche de provoquer ce bug.

Les classes d'implémentations des balises ```click``` et ```clickStep``` ont été modifiées pour utiliser ```ClickMouseEventData``` au lieu de ```MouseEventData```.

**Cas particulier de la balise** ```**clickTableHeader**``` : Capri plantant pour une raison inconnue sur cette balise suite à la modification décrite ci-dessus, cette step instancie le ```MouseEventData``` d'origine. Ceci a été rendu possible par le biais d'une méthode ```createMouseEventData dans AbstractClickStep``` surchargée dans ```ClickTableHeaderStep```.
