---
layout: post
title: agf-datagen - Gestion multibases des handlers
tags: [codjo-datagen,framework-1-51]
---
Mise à jour des ```handler-select```, ```handler-update```, ```handler-requetor``` et ```handler-sql``` pour être compatible Oracle (utilisation des méthodes ```computedRowCount(...)``` de ```QueryUtil``` localisées dans ```codjo-mad```) .
