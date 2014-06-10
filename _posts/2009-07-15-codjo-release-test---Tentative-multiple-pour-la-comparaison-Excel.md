---
layout: post
title: agf-release-test - Tentative multiple pour la comparaison Excel
tags: [framework-1-103,codjo-release-test]
---
Afin d'éviter l'erreur "Workbook nb=0", nous avons ajouté un comportement permettant à la balise ```assertExcel``` de réessayer son test pour une durée pré-déterminée.

Par contre, nous avons constaté que cette modification corrigeait de façon aléatoire le problème. 

{info} Développement exploratoire pour stabiliser SIC{info}