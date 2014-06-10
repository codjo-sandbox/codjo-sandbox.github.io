---
layout: post
title: agf-security - Préparation au support multi-base
tags: [codjo-security,framework-1-49]
---
Lors de l'enregistrement du modèle security, deux requêtes étaient envoyées à la BD en même temps. Mais ceci n'est pas compatible avec Oracle. Les deux requêtes sont exécutées l'une après l'autre.