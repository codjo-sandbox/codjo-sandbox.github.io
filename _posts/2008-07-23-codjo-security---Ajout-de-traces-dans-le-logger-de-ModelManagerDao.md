---
layout: post
title: agf-security - Ajout de traces dans le logger de ModelManagerDao
tags: [framework-1-54,codjo-security]
---
Une clause **catch** sur une **SQLException** a été ajoutée dans les méthodes ```deleteSecurityModel``` et ```saveModel``` de la classe ```ModelManagerDao``` afin de logguer en erreur d'éventuels problèmes de suppression ou de sauvegarde du modèle de sécurité.