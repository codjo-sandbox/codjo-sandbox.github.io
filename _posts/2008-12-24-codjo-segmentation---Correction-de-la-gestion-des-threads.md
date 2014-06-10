---
layout: post
title: agf-segmentation - Correction de la gestion des threads
tags: [framework-1-77,codjo-segmentation]
---
Lors de l'import et de l'export de paramétrage, certaines modifications d'IHM étaient effectuées dans un thread différent du Swing Thread (cf. [[swdev:Swing et les threads]]).

Ce bug causait de manière aléatoire des erreurs lors des tests d'intégration.

