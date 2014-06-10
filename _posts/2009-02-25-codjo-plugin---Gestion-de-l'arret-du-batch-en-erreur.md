---
layout: post
title: agf-plugin - Gestion de l'arrêt du batch en erreur
tags: [framework-1-84,codjo-plugin]
---
Le batch ne s'arrêtait pas en cas d'exception pendant la phase de "start". A présent, si un tel cas se produit, l'erreur est loggée et le process sort avec un code d'erreur spécifique à 50.