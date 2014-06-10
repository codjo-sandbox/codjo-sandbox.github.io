---
layout: post
title: agf-release-test - Correction technique mineure sur la balise AssertExcel
tags: [framework-1-111,codjo-release-test]
---
Le mécanisme de répétition de la balise ```assertExcel```, qui teste qu'il y a au moins un fichier Excel ouvert, a été déporté dans une classe à part. 
Des tests unitaires ont été créés pour valider le mécanisme de répétition.
