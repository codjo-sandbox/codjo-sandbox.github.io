---
layout: post
title: agf-database -  Avertissement en cas de mauvaise configuration
tags: [framework-1-54,codjo-database]
---
Une application voulant utiliser ```codjo-database``` mais n'ayant pas configuré la dépendance vers ```agf-database-main``` génèrera une exception au moment de l'appel à _new DatabaseFactory()_.
Le message d'erreur a été changé et renvoie désormais :
```"Aucune base n'est configurée. Vérifiez votre dépendance vers codjo-database-main"```.