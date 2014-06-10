---
layout: post
title: agf-mad - Correction du redimensionnement de la popup de la RequestComboBox
tags: [framework-1-66,codjo-mad]
---
Le redimensionnement de la popup de la RequestComboBox se déclenchera uniquement après un chargement des données (appel à la méthode ```load()```).
Le redimensionnement se fait maintenant aussi sur la hauteur.
Le redimensionnement en largeur a aussi été corrigé pour prendre en compte, quand il le faut, la largeur de la ```ScrollBar```.