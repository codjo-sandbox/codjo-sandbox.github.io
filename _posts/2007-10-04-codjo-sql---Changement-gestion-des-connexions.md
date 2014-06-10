---
layout: post
title: agf-sql - Changement gestion des connexions
tags: [codjo-sql,framework-1-15]
---
Dans la classe ```ConnectionPool```, changement de la stratégie de libération des connexions non utilisés. 

Avant les connexions étaient libérées une à une en fonction d'un timeout de pool, maintenant chaque connexion possède son propre timeout réglé sur 15 secondes par défaut.

