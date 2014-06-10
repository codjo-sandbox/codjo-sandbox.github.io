---
layout: post
title: agf-sql - Implementation du stop sur le plugin JdbcServerPlugin
tags: [codjo-sql,framework-1-15]
---
Maintenant le plugin ```JdbcServerPlugin``` ferme correctement tous les pools de connexion encore actif lors de l'arrêt du socle (méthode ```stop```).
