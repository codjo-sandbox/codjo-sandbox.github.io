---
layout: post
title: agf-workflow  - Problème d'abandon de la requete obsolete
tags: [framework-1-19,codjo-workflow]
---
Il semble que ce problème soit du à la dérive des horloges des clients et du serveur.

Correction temporaire : augmentation du timeout de réponse (REPLY_TIMEOUT monté à 4 minutes).