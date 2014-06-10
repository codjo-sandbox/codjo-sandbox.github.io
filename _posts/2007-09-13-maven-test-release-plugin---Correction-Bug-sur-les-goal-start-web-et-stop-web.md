---
layout: post
title: maven-test-release-plugin - Correction Bug sur les goal start-web et stop-web
tags: [maven-test-release-plugin,framework-1-12]
---
\- Les mojos sus-cités ne se lancent que si le Include web de la configuration du plugin dans le module test-release de l'application en question est présent.