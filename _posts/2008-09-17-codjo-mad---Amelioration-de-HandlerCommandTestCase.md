---
layout: post
title: agf-mad - Amélioration de HandlerCommandTestCase
tags: [framework-1-62,codjo-mad]
---
Dans la classe HanlderCommandTestCase, si une exception était levée lors du chargement du fichier tokio, elle n'était pas remontée et ne bloquait pas l'exécution du test.

A présent, l'exception est remontée.