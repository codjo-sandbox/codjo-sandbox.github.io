---
layout: post
title: agf-workflow - Correction sur la sortie en erreur d'un batch
tags: [framework-1-62,codjo-workflow]
---
Le problème provenait de la méthode ```printStackTrace``` de la classe ```JobBatchException``` qui renvoyait un ```NullPointerException``` lorsque l'on n'avait pas de description sur l'erreur.

Cette correction permet aux scripts KSH des batchs de récupérer le bon code d'erreur et d'avoir des fichiers logs complets.