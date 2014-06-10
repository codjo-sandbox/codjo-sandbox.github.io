---
layout: post
title: agf-mad - Audit des handlers
tags: [framework-1-93,codjo-mad]
---
Il est maintenant possible d'enregistrer des statistiques d'exécution des handlers.
Ces statistiques comprennent le temps d'exécution du handler, le temps d'exécution de chaque requête BD et le nombre de connexions libres/utilisées avant l'exécution du handler.

Par défaut, cet audit est désactivé. Afin de l'activer, il faut passer par le plugin ```AdministrationServerPlugin``` (cf. [[/2009/04/28/codjo-administration - Activation des logs sur les handlers]]).
