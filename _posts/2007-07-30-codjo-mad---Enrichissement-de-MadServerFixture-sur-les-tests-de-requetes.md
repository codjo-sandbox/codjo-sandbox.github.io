---
layout: post
title: agf-mad - Enrichissement de MadServerFixture sur les tests de requêtes
tags: [codjo-mad,framework-1-8]
---
Ajout d'un MadServerFixture.assertSentRequests pour tester les requêtes envoyées via Mad.
Ajout d'un reset sur le RequestIdManager pour pouvoir tester correctement les requêtes.