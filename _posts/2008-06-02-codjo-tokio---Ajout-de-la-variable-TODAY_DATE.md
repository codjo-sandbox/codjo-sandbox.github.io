---
layout: post
title: agf-tokio - Ajout de la variable TODAY_DATE
tags: [framework-1-46,codjo-tokio]
---
Ajout de la variable TODAY_DATE qui s'utilise de la même manière que TODAY.
La différence est que TODAY_DATE renvoie la date du jour sous la forme yyyy-MM-dd 00:00:00.0, c'est à dire avec les heures, les minutes et les secondes à zero.

Il est possible d'ajouter ou de soustraire des jours, des mois et des années.

Exemple:
```
<field name="ISR_DDAT_ID" value="TODAY_DATE-1D"/>
```

Le champ ISR_DDAT_ID contiendra la date du jour - 1 jour