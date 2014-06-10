---
layout: post
title: agf-workflow - Création de plugin workflow de type batch
tags: [framework-1-101,codjo-workflow,hot-topics]
---
2 classes ont été ajoutées afin de faciliter la création d'un plugin workflow de type batch :
- ```AbstractWorkflowBatchPlugin``` : cette classe regroupe les caractéristiques communes d'un workflow de type batch (configuration, démarrage, exécution, arrêt) et propose que ses sous-classes concrètes implémentent la méthode ```createRequest``` contenant la partie spécifique du traitement à effectuer,
- ```WorkflowBatchPluginConfiguration``` : cette classe correspond à la configuration du workflow de type batch.

Cela a permis de supprimer de nombreuses duplications au niveau applicatif et framework (```codjo-imports``` et ```agf-broadcast```).

Cette news est en relation avec les news suivantes :
[[/2009/06/19/codjo-broadcast - Refactoring batch broadcast]]
[[/2009/06/19/codjo-imports - Refactoring batch import]]