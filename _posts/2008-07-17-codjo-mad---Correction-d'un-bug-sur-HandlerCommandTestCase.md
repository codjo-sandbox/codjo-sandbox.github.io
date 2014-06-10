---
layout: post
title: agf-mad - Correction d'un bug sur HandlerCommandTestCase
tags: [framework-1-53,codjo-mad]
---
Un bug sur ```HandlerCommandTestCase``` a été introduit lors du découpage d'```codjo-test``` et de l'extraction de ```JdbcFixture```.
La base de données utilisée était celle de la ```lib``` au lieu d'être celle de ```dev```. Cela a été corrigé.