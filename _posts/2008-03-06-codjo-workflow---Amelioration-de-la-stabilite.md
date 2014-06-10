---
layout: post
title: agf-workflow - Amélioration de la stabilité
tags: [codjo-workflow,framework-1-34]
---
Prise en compte des cas d'echec non prévu par une implémentation spécifique d'un ```JobAgent```. Un ```catch(Throwable)``` capture toutes les exceptions, ce qui évite un blocage du processus. Ce processus est alors déclaré en erreur et l'exception est remontée au client.

**NB** : Ce bug était visible dans le cas d'un export ayant une expression invalide. Dans ce cas, le process batch restait bloqué.