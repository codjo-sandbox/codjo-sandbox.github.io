---
layout: post
title: agf-security - Correction de la gestion du timestamp de mise-à-jour de PM_SEC_MODEL
tags: [framework-1-70,codjo-security]
---
La timestamp indiquant la date de mise-à-jour du modèle de sécurité en base n'était pas correctement modifié. 

Ce problème n'était visible que dans le cadre d'une utilisation des plugin sécurité sur des clients lourds (client/server).
