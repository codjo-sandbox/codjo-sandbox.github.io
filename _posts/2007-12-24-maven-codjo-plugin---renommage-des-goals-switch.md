---
layout: post
title: maven-agf-plugin - renommage des goals switch
tags: [maven-codjo-plugin,framework-1-25,hot-topics]
---
Les deux goals _switch_ ont été renommés pour supprimer les références au mot lib (ces deux goals portant aussi bien sur des lib que sur des plugins), il faut donc utiliser maintenant :
** **```agf:switch-to-snapshot```* : bascule une librairie ou un plugin en SNAPSHOT (à jouer dans le pom parent),
** **```agf:switch-to-release```* : remplace toutes les occurences des librairies en snapshot par leur version stabilisée attendue.

