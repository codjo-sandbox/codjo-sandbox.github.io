---
layout: post
title: agf-broadcast - Refactoring batch broadcast
tags: [framework-1-101,codjo-broadcast]
---
Les évolutions apportées à la lib ```workflow``` mentionnées dans la news [[/2009/06/19/codjo-workflow - Création de plugin workflow de type batch]] ont été reportées au niveau de la lib broadcast :
- refactoring de la classe ```BroadcastBatchPlugin``` afin de dériver de la classe ```AbstractWorkflowBatchPlugin```,
- suppression de la classe ```BroadcastBatchPluginConfiguration```.