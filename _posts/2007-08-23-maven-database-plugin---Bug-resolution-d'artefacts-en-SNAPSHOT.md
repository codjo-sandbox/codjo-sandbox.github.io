---
layout: post
title: maven-database-plugin - Bug résolution d'artefacts en SNAPSHOT
tags: [maven-database-plugin,framework-1-10]
---
Correction du bug lors de la résolution des artefacts sur dépot distant.

Lorsqu'on spécifie dans la configuration de maven-database-plugin un <include> vers un artefact en version SNAPSHOT, le plugin fait maintenant correctement la résolution vers la dernière version timestampée correspondante.