---
layout: post
title: agf-test - Optimisation de la classe TokioFixture
tags: [codjo-test,framework-1-37]
---
La classe ```TokioFixture``` a été optimisé. 

<u>Maintenant</u> : 
* Le fichier Tokio n'est plus chargé dans le constructeur mais lors du ```doSetup()``` : Ce qui réduit considérablement la trace mémoire utilisée lors de l'exécution des tests en masse (e.g. Maven).
* Le fichier Tokio n'est plus re-chargé si il a été précédemment chargé (comparaison avec le ```lastLoadedTokioFile```).

