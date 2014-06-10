---
layout: post
title: maven-test-release-plugin - Serveur local non arrêté
tags: [framework-1-92,maven-test-release-plugin]
---
Lors d'un build en ```-Dprocess=integration -Dcoverage=true``` et en serveur local, si des ```tests-release``` étaient en échec, le serveur n'était pas correctement stoppé.

Cela a été corrigé.