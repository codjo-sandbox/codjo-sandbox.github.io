---
layout: post
title: agf-datagen - Correction génération du handler update gérant historic-audit-trail
tags: [codjo-datagen,framework-1-79]
---
Une correction a été apportée lors de la génération du handler update. Lorsque le handler-update était redéfini et que la feature historic-audit-trail était précisée, le handler ne compilait pas car il manquait un import vers la librairie castor.