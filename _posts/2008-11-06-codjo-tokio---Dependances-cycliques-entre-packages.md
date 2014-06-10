---
layout: post
title: agf-tokio - Dépendances cycliques entre packages
tags: [framework-1-68,codjo-tokio]
---
La mise en place des tests de dépendances a permis la détection d'une dépendance cyclique entre les packages ```com.agf.tokio``` et ```com.agf.tokio.util```. 

```ScenarioBuilder``` (la classe incriminée) a été déplacée.