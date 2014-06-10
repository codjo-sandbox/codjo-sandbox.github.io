---
layout: post
title: agf-datagen - Correction delete-handler (multibase)
tags: [codjo-datagen,framework-1-79]
---
Pour la gestion de la feature **historic-audit-trail**, le **handler-delete** généré utilisait une fonction **getDate()** spécifique à Sybase. Cette spécificité a été remplacée par un code plus générique.