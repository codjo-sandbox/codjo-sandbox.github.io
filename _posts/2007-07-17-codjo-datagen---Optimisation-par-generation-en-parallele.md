---
layout: post
title: agf-datagen - Optimisation par génération en parallèle
tags: [framework-1-5,codjo-datagen]
---
Optimisation du traitement par une mise en parallèle de la génération.

Chaque générateur (Handler, table, etc) est éxécuté dans un ```thread``` différent.
