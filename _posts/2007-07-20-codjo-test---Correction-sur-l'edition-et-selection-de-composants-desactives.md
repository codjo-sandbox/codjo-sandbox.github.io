---
layout: post
title: agf-test - Correction sur l'édition et sélection de composants désactivés
tags: [codjo-test,framework-1-6]
---
Les steps **select**, **setValue** et **editCell** ne prenaient pas en compte l'état **désactivé** du composant traité et donc permettaient l'édition de ce dernier. A présent, une exception de type **GuiConfigurationException** sera lancée avec comme message d'erreur '_Le composant 'xxx' n'est pas éditable_'.