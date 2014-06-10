---
layout: post
title: agf-tokio - Refactoring de TokioFixture
tags: [framework-1-93,codjo-tokio]
---
```TokioFixture``` a été remanié suite au chantier ```multi-bases```.
Le ```JdbcFixture``` utilisé est dorénavant construit via database et à partir des fichiers ```database.properties``` ou ```tokio.properties```.