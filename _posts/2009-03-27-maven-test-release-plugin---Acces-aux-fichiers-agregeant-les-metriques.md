---
layout: post
title: maven-test-release-plugin - Accès aux fichiers agrégeant les métriques
tags: [framework-1-89,maven-test-release-plugin]
---
Précédemment, lorsque plusieurs processus d'intégration mettaient à jour  les fichiers agrégeant les métriques (metrics-basic.xls et metrics-coverage.xls) en même temps, les lignes pouvaient être mélangées.

L'accès aux fichiers est maintenant protégé par un système de lock.