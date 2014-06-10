---
layout: post
title: maven-agf-plugin - Correction bug dépendances modules
tags: [maven-codjo-plugin,framework-1-21]
---
Correction d'un bug de non prise en compte des dépendances dans les modules lors de l'utilisation des goals de switch des librairies en release ou en snapshot.

Désormais, lors de l'utilisation des goals ```mvn agf:switch-lib-to-release``` et ```mvn agf:switch-lib-to-snapshot``` l'ensemble des dépendances et des plugins spécifiés dans les modules dépendant du pom-parent sont traitées de la même manière que s'il était spécifié dans le pom-parent. 

