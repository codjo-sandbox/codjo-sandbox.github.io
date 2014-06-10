---
layout: post
title: agf-security - Correction de la date minimum pour la compatibilité SyBase - MySQL
tags: [framework-1-63,codjo-security]
---
Dans le cadre de la gestion de base de donnée MySQL:
La date minimale (type **TIMESTAMP**) est 1970-01-01 00:00:01 UTC/GMT
Or, pour éviter les problèmes de décalage horaire, on définit la date minimale à 1970-01\-**02** 00:00:00.

Cette correction a été apportée pour l'initialisation de la table PM_SEC_MODEL (classe ModelManagerDao) .