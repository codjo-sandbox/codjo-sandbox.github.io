---
layout: post
title: agf-pom - Jar jconnect non présent dans la livraison
tags: [framework-1-56,codjo-pom]
---
Lors de livraisons d'applications standalone (Iris notamment), ```jconnect``` n'était pas packagé.
Cela a été résolu en passant la dépendance ```jconnect``` de runtime en compile.