---
layout: post
title: maven-test-release-plugin - Arrêt du serveur après test spécifique
tags: [maven-test-release-plugin,framework-1-7]
---
Le serveur n'est plus stoppé si un test-release échoue dans le cas où ce test avait été demandé explicitement par l'intermédiaire de l'option -Dtest=...

voir [[/2007/06/29/maven-test-release-plugin - Exécution d'un ensemble de TR en ligne de commande]]