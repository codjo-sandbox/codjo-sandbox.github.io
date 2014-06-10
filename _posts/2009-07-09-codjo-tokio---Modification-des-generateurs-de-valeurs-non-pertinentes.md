---
layout: post
title: agf-tokio - Modification des générateurs de valeurs non pertinentes
tags: [framework-1-104,codjo-tokio,kaizen-tr]
---
{info:title=Dans le cadre du Kaizen TR}{info}

Un nouveau générateur, ```generateInt``` a été mis en place.
De plus, le générateur ```generateTimestamp``` a été supprimé car il était redondant avec ```generateDateTime```.

[[Voir Doc | codjo-tokio - Fonctions de génération de valeurs]]