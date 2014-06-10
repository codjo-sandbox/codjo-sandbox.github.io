---
layout: post
title: agf-tokio - Amélioration de TokioFixture
tags: [framework-1-62,codjo-tokio]
---
**{<u>}Contexte{</u>}** :

La classe **TokioFixture** supporte le chargement de fichiers d'extensions _".tokio"_ et _".xml"_&nbsp; dans le cas où la résolution du nom du fichier _".tokio"_ se fait à partir du nom de la classe de test. Le _load_ essaye d'abord de charger un _".tokio"_ et si une exception est levée il essaye de charger un _".xml"_.

Cette mécanique masquait les exceptions de chargement de fichier _".tokio"_ donc les exceptions levées ne concernaient plus le chargement du fichier ".tokio" mais celui du fichier ".xml". Dès lors l'exception apparaissant dans la console ne précisait pas l'origine exacte de l'erreur.


**{<u>}Correction{</u>}** :

A présent on vérifie quel type de fichier est chargé&nbsp; _".tokio"_ ou _".xml"_, et on procède au chargement.

Toute exception levée lors du chargement est à présent encapsulée dans une **TokioLoaderException**.
\\ \\