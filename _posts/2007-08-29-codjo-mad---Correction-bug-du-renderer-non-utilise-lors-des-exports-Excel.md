---
layout: post
title: agf-mad - Correction bug du renderer non utilisé lors des exports Excel
tags: [framework-1-10,codjo-mad]
---
Le renderer d'affichage des données n'était pas toujours utilisé lors de l'export excel, comme dans la cas du PreferenceRenderer. Donc dans certain cas les informations exportées ne correspondaient pas à ce qui était affiché.
(Exemple : Dans une RequestTable il y avait affiché 0.0000000000000 dans une cellule, mais 0E-13 était exporté. )