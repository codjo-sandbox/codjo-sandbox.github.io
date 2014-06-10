---
layout: post
title: agf-sql - Consolidation du ConnectionSpy
tags: [framework-1-93,codjo-sql]
---
Le ```ConnectionSpy``` pouvait lancer des exceptions dans certains cas.
Désormais, il n'en renvoie plus car ce n'est pas son rôle.