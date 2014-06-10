---
layout: post
title: agf-segmentation - Augmentation de la taille de la variable pour l'expression principale
tags: [framework-1-19,codjo-segmentation]
---
La taille de la variable locale dans laquelle on stockait l'expression principale de PM_EXPRESSION a été augmentée de varchar(3000) à varchar(15000) pour pouvoir accepter un plus grand nombre de poches dans un axe.