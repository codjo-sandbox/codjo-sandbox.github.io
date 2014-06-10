---
layout: post
title: agf-sql - Gestion du CallableStatement en MySQL
tags: [codjo-sql,framework-1-83]
---
En attendant la reprise du chantier "Multi-bases", une modification temporaire a été effectuée dans la classe ConnectionPool. Dans le cas d'une connexion MySQL, cette modification ajoute une propriété "noAccessToProcedureBodies" fixée à ```true``` de façon à pouvoir utiliser des ```CallableStatement```.