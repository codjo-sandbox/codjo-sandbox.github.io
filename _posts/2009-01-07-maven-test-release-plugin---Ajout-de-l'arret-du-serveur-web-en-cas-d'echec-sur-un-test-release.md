---
layout: post
title: maven-test-release-plugin - Ajout de l'arrêt du serveur web en cas d'échec sur un test release
tags: [framework-1-78,maven-test-release-plugin]
---
Auparavant, seul l'arrêt du serveur jade était déclenché si une exception était levée dans la tâche **RunMojo** (tâche exécutant les tests release).

Maintenant, l'arrêt du serveur web est déclenché aussi. 