---
layout: post
title: agf-crypto - Meilleure gestion de l'UTF-8 sur le cryptage
tags: [framework-1-78,codjo-crypto]
---
Lorsque l'on retournait la chaine de caractères encryptée, on ne reprécisait pas l'encodage en ```UTF-8```. Ce n'était pas homogène par rapport aux autres manipulations effectuées sur les chaines de caractères notamment en décryptage.