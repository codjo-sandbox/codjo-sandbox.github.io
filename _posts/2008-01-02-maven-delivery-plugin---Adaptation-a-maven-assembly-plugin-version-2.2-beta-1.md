---
layout: post
title: maven-delivery-plugin - Adaptation à maven-assembly-plugin version 2.2-beta-1
tags: [maven-delivery-plugin,framework-1-25]
---
Le code a été réécrit pour être compatible avec la nouvelle version du plugin maven.

Des filtres sur les fichiers ```*.sh``` ont été ajoutés dans le fichier ```server.xml``` pour remplacer la sélection sur le fichier ```server.sh```.