---
layout: post
title: maven-test-release-plugin - Amélioration de la collecte des metrics
tags: [framework-1-87,maven-test-release-plugin]
---
Une version synthétique des métriques de toutes les applications est produite dans les fichiers suivants : 

* ```Z:\equipes\kaizen-tr\metrics\metrics-basic.xls``` : contient les métriques basiques (nombre de TR, durée d'éxecution, etc.)
* ```Z:\equipes\kaizen-tr\metrics\metrics-coverage.xls``` : contient les métriques de couverture de code (pourcentage de code couvert, etc.)


{info:title=Attention}
Pour éviter de locker les fichiers, et donc empêcher les process SIC d'écrire dedans, il faut copier les fichiers localement pour les regarder.
{info}