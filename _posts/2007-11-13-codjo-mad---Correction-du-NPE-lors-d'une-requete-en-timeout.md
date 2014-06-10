---
layout: post
title: agf-mad - Correction du NPE lors d'une requête en timeout
tags: [codjo-mad,framework-1-19]
---
L'exception ```NullPointerException``` est remplacé par une ```RequestException``` avec le message suivant : "```Erreur de communication avec le serveur: Il n'a pas répondu dans le temps imparti.```".