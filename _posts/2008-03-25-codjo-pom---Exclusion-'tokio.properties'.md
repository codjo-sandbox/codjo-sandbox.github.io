---
layout: post
title: agf-pom - Exclusion 'tokio.properties'
tags: [codjo-pom,framework-1-36]
---
L'exclusion des ```tokio.properties``` a été remonté dans le ```super-pom``` racine. Cela permet de traiter le cas des applications produisant un jar de test.

**Donc** les ```tokio.properties``` ne sont plus présent dans les jar de type classifier ```test```.
