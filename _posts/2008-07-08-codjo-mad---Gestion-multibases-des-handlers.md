---
layout: post
title: agf-mad - Gestion multibases des handlers
tags: [codjo-mad,framework-1-51]
---
Introduction d'une méthode protégée (```computedRowCount(con, query, idx)```) sur la classe ```QueryUtil```.

Cette méthode permet de calculer le nombre de lignes impactées par la requête dans les classes abstraites des handler (e.g. calcule le nombre de lignes total résultant d'un select).

Cette méthode est notamment utilisée par ```AbstractRequetorHandler``` et ```AbstractSqlHandler```.
