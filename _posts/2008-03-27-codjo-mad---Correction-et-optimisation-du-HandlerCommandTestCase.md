---
layout: post
title: agf-mad - Correction et optimisation du HandlerCommandTestCase
tags: [codjo-mad,framework-1-37]
---
Le ```HandlerCommandTestCase``` a été corrigé pour prendre en compte l'optimisation du ```TokioFixture``` (chargement lazy du fichier Tokio).

De plus, un seul ```JdbcFixture``` est construit à la place de 2 précédemment.

