---
layout: post
title: agf-mad - Uniformisation du contrat de getRow() de Result
tags: [framework-1-62,codjo-mad]
---
La méthode ```Result.getRow(index)``` retourne maintenant tout le temps une ```IndexOutOfBoundsException``` lorsque l'index est incohérent. Avant elle retournait un pointeur null dans certains cas.
