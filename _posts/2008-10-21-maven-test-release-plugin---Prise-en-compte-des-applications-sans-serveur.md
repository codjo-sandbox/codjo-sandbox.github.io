---
layout: post
title: maven-test-release-plugin - Prise en compte des applications sans serveur
tags: [framework-1-67,maven-test-release-plugin]
---
Les goals ```start-server```, ```stop-server``` et ```deliver-server``` ne se déclenchent plus si le projet ne possède pas de server. Le fonctionnement devient identique aux goals ```start-web``` et ```stop-web```.

