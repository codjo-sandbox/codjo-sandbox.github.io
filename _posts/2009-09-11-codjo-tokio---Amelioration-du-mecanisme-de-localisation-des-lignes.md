---
layout: post
title: agf-tokio - Amélioration du mécanisme de localisation des lignes
tags: [framework-1-113,codjo-tokio]
---
* La librairie a été modifiée afin de permettre l'affichage de liens vers les fichiers ```tokio``` dans la console lors de l'exécution de tests releases.
* La trace d'une ```row``` venant d'un ```required``` donnera ceci : ```row-required(myFile.tokio:77)```.
* La trace d'une ```row``` héritant d'une ```row``` d'un ```scenario``` donnera ceci : ```row-inherited(myFile.tokio:77)```.
* Quelques bugs liés à la localisation des lignes ont été corrigés.