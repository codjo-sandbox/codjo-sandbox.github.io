---
layout: post
title: agf-tokio - Problème de mémoire avec TokioFixture
tags: [framework-1-110,codjo-tokio]
---
Après avoir appelé ```TokioFixture.doTearDown()```, des références vers des objets inutilisés persistaient.
Cela pouvait provoquer des problèmes de mémoire lors de l'exécution des tests avec ```maven```.

Cela a été corrigé.