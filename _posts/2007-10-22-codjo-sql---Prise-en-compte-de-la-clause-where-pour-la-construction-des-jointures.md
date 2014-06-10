---
layout: post
title: agf-sql - Prise en compte de la clause where pour la construction des jointures
tags: [framework-1-17,codjo-sql]
---
Actuellement les jointures sont construites ou non en fonction des champs ramenés par le select.
Désormais, cette construction prend également en compte les champs de la clause where, du group by, etc... 