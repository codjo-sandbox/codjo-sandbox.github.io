---
layout: post
title: agf-sql - Arrêt immédiat de la connexion à la base lors de la fermeture du client
tags: [framework-1-86,codjo-sql,hot-topics]
---
<u>Problème</u>

Lors de l'arrêt d'un client les traitements BD en cours bloquaient la fermeture de la connexion vers celle-ci. Dès lors toute tentative de création de nouvelle connexion était mise en attente. Ce qui pouvait amener par exemple à un timeout.

<u>Solution</u>

L'arrêt de la connexion BD est maintenant forcé et est donc immédiat. 

