---
layout: post
title: agf-tokio - Contrôle des paramètres invalides dans les entités
tags: [framework-1-70,codjo-tokio]
---
Un contrôle vérifie que les paramètres spécifiés dans un **<create-entity>** sont présents dans la définition de l'entité.

Dans le cas ou un paramètre illégal a été saisi, une exception est levée.