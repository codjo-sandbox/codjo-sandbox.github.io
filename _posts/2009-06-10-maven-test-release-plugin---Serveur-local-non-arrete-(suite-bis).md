---
layout: post
title: maven-test-release-plugin - Serveur local non arrêté (suite bis)
tags: [framework-1-99,maven-test-release-plugin,resolution-of-brin]
---
Après analyse des traces laissées lors de l'arrêt des serveurs locaux (cf. [[/2009/04/27/maven-test-release-plugin - Serveur local non arrêté (suite)]]), nous avons fait les modifications suivantes :
* l'arrêt du serveur n'est plus exécuté dans un ```EmmaJavaExecutor``` mais dans un ```DefaultJavaExecutor```,
* le timeout d'arrêt du serveur local a été monté à 60s,
* le paramètre ```-Dlog.dir=``` a été ajouté au lancement du serveur local.

{note:title=Eradication de B.R.I.N. en cours}{note}