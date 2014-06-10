---
layout: post
title: agf-segmentation - Déclenchement des tests release
tags: [codjo-segmentation,framework-1-30]
---
Les tests release sont déclenchés lors de l'```install``` du module ```release-test```.

La classe de test unitaire ```AllReleaseTest```, qui a en charge de lancer tous les tests release, ne peut pas être exécutée depuis IntelliJ.