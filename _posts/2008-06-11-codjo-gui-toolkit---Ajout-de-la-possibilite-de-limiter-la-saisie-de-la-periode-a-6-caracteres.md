---
layout: post
title: agf-gui-toolkit - Ajout de la possibilité de limiter la saisie de la période à 6 caractères
tags: [codjo-gui-toolkit,framework-1-48]
---
Le composant graphique ```PeriodField``` peut désormais être initialisé avec une option permettant de restreindre ou non le nombre des caractères saisis. Par défaut, la saisie est limitée à 6 caractères.

Ex : 

```
PeriodField periodField = new PeriodField(); // Saisie limitée à 6 caractères
PeriodField periodField = new PeriodField(true); // idem
PeriodField periodField = new PeriodField(false); // Saisie non limitée
```
