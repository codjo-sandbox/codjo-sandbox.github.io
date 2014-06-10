---
layout: post
title: agf-imports - Refactoring batch import
tags: [framework-1-101,codjo-imports]
---
Les évolutions apportées à la lib ```workflow``` mentionnées dans la news [[/2009/06/19/codjo-workflow - Création de plugin workflow de type batch]] ont été reportées au niveau de la lib imports :
- refactoring de la classe ```ImportBatchPlugin``` afin de dériver de la classe ```AbstractWorkflowBatchPlugin```,
- suppression de la classe ```ImportBatchPluginConfiguration```.