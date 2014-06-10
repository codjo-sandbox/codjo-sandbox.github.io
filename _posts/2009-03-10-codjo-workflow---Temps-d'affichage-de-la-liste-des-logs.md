---
layout: post
title: agf-workflow - Temps d'affichage de la liste des logs
tags: [framework-1-86,codjo-workflow,hot-topics]
---
Afin d'améliorer le temps de chargement de l'IHM des logs, le handler ```selectAllWorflowLog``` a été modifié. Il ne ramène plus que les colonnes utilisées dans l'affichage de la liste.

Pour info, avec 18 000 lignes de log le temps d'ouverture est passé de **15,4** à **1,7** secondes.