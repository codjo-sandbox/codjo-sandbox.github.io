---
layout: post
title: agf-test - Ajout du mode pour les balises relatives au JTree
tags: [codjo-test,framework-1-18]
---
Ajout de l'attribut mode pour les balises relatives au JTree : select, clickRight, assertTree
Deux valeurs sont possibles pour cet attribut : "display" (par défaut) et "model"
La valeur "model" se base sur le toString() des userObject contenus dans le JTree.
La valeur "display" se base sur les renderers.
