---
layout: post
title: agf-aspect - Correction sur AbstractSqlAspect et AbstractBasicSqlAspect
tags: [framework-1-78,codjo-aspect]
---
La clôture des statements dans le bloc ```finally``` de la méthode ```runSql``` des classes ```AbstractSqlAspect``` et ```AbstractBasicSqlAspect``` comportait un bug dans le cas où le contenu des scripts SQL définis dans les classes concrètes était hétérogène. Ce bug a été corrigé.