---
layout: post
title: agf-plugin - Amélioration de l'inversion de contrôle des socles
tags: [framework-1-109,codjo-plugin,hot-topics]
---
Deux nouvelles méthodes facilitant la gestion IoC ([[Inversion of Control|http://fr.wikipedia.org/wiki/Inversion_de_contr%C3%B4le]]) ont été ajoutées aux socles (c.a.d. ```ApplicationCore```) :
* ```void addGlobalComponentImplementation(Class)``` : permet d'ajouter un composant au conteneur IoC (Pico). Le composant ne sera instancié qu'à la demande,
* ```MutablePicoContainer createChildPicoContainer()``` : permet d'instancier un nouveau conteneur fils du conteneur parent.

Exemple d'utilisation [[ici|codjo-mad - Handler construction principle]].