---
layout: post
title: agf-broadcast - Correction sur l'IHM des selectors génériques
tags: [framework-1-104,codjo-broadcast]
---
Les selectors génériques sont éditables via une IHM (il s'agit d'une requète SQL saisie dans un champ texte). Ensuite une section d'export peut être rattachée à ce type de selector. 

Dans le cas où l'utilisateur voulait supprimer ce selector générique, le système vérifiait s'il n'était pas rattaché à une section et renvoyait un message d'erreur dans ce cas-là. Cependant l'autre cas (selector non rattaché) ne marchait pas.