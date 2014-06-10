---
layout: post
title: agf-release-test - AssertTableExcel gestion des formats de cellule excel
tags: [framework-1-52,codjo-release-test]
---
Il est désormais possible d'utiliser d'autres formats de cellule que le format texte dans les fichiers excel d'étalon lors de l'utilisation de la balise AssertTableExcel.

Concernant les dates, les formats suivant sont gérés :
* 10/01/2068
* 25/12/06
* Wed Dec 24 00:00:00 CET 2008

Les formules de calcul sont également gérées.