---
layout: post
title: agf-sql - Identification des connexions pour une application
tags: [framework-1-12,codjo-sql]
---
Les connexions crées par un ```ConnectionPool``` sont identifiables par le nom de l'application. C'est-à-dire le champ ```APPLICATIONNAME``` d'une connexion est rempli avec l'identifiant de la plateforme (e.g. "gabi-1.00.00.00-a-SNAPSHOT").

Maintenant il est donc possible d'identifier rapidement les connexions en BD via la commande SQL suivante :
```sql


