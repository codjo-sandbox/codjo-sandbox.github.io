---
layout: post
title: agf-datagen - Correction de la génération en multithread
tags: [framework-1-5,codjo-datagen]
---
La génération multithreading est maintenant corrigée. Le bug venait du fait que parfois java ne pouvait pas créer les répertoires destination. Le problème a été résolu en forçant la création par tentatives successive.