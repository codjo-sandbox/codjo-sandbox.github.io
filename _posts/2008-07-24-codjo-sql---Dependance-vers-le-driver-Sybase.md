---
layout: post
title: agf-sql - Dépendance vers le driver Sybase
tags: [framework-1-54,codjo-sql]
---
Il existe dans le code un chargement dynamique du driver Sybase, quelle que soit la base de données configurée.
Une dépendance vers le driver jconnect a été explicitement ajoutée.
Cette modification est temporaire, le temps du passage en full multibase.
