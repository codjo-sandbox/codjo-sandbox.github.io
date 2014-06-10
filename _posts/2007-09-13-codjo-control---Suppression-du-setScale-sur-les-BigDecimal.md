---
layout: post
title: agf-control - Suppression du setScale sur les BigDecimal
tags: [codjo-control,framework-1-12]
---
En raison d'un vieux bug weblogic on imposait une limitation sur les BigDecimal setScale(9), elle est maintenant inutile.