---
layout: post
title: maven-database-plugin - Suppression de la dépendance à agf-common
tags: [maven-database-plugin,framework-1-27]
---
Suppression de la dépendance vers la librairie codjo-common en remplacant l'utilisation de la classe ```FileUtil``` de ```agf-common``` par celle de la classe ```FilesUtils``` de ```plexus```.
