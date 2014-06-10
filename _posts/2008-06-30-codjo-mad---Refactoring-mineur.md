---
layout: post
title: agf-mad - Refactoring mineur
tags: [codjo-mad,framework-1-50]
---
Déplacement de la méthode ```replaceUser``` de la classe ```AbstractSqlHandler``` vers la classe utilitaire ```QueryUtil```.

Pour information, cette méthode est utilisée par les handlers pour remplacer la chaîne ```$user$``` par ```'currentLogin'``` (où ```currentLogin``` désigne le login de l'utilisateur courant).

