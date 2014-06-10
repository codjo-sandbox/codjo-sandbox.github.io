---
layout: post
title: agf-database - Ordonnancement des tables indépendant de la casse
tags: [framework-1-62,codjo-database]
---
Le tri des tables en fonction des contraintes est maintenant indépendant de la casse. 

Ce mécanisme est notamment utilisé par [[codjo-tokio]] pour déterminer l'ordre des truncate/insert.
