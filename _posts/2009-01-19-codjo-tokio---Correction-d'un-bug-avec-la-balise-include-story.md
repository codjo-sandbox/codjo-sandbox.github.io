---
layout: post
title: agf-tokio - Correction d'un bug avec la balise include-story
tags: [framework-1-80,codjo-tokio]
---
En utilisant ```<include-story>```, il n'était pas possible de faire des remplacements de variable (```$\{ma.variable\```} par exemple) dans les fichiers tokios inclus.
Cela a été corrigé.