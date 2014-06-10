---
layout: post
title: agf-release-test - Fermeture d'excel
tags: [framework-1-72,codjo-release-test]
---
A l'exécution de tests utilisant la balise ```assert-excel```, Excel n'était pas toujours fermé.

Afin de minimiser ce problème (et n'ayant pas été possible de faire autrement) des ```sleeps``` ont été ajoutés, permettant de réduire le nombre de problèmes de fermeture d'Excel.
