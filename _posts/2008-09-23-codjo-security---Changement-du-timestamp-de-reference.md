---
layout: post
title: agf-security - Changement du timestamp de référence
tags: [framework-1-62,codjo-security]
---
La date de référence (désignant le premier timestamp) utilisée par la couche de sécurité a été modifiée. Précédemment elle était fixée à la date UTC (i.e. '1970-01-01 00:00:00.0'). Pour des raisons de compatibilité avec MySql, elle est passée à UTC + 1s (i.e. '1970-01-01 00:00:01.0').

Cette date est notamment utilisée lors du premier enregistrement du modèle de sécurité en BD.
