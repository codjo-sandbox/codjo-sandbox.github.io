---
layout: post
title: agf-release-test - Gestion des Colonnes sans header dans la comparaison JTable vs Excel
tags: [framework-1-53,codjo-release-test]
---
Dans certains JTreeTables certaines colonnes n'ont pas de headers.
Désormais, la recherche de la colonne teste la nullité de ce header pour éviter le NullPointerException.