---
layout: post
title: agf-workflow - Création des audits de tâches dans des méthodes séparées
tags: [framework-1-115,codjo-workflow]
---
Deux méthodes ```create...Audit``` ont été créées dans la classe ```JobProtocolParticipant``` pour faciliter la surcharge des méthodes ```handlePRE(JobRequest)``` et ```handlePOST(JobRequest, JobException)``` :
* ```createPreAudit(JobRequest)``` crée le ```JobAudit``` de type ```PRE```
* ```createPostAudit(JobRequest, JobException)``` crée le ```JobAudit``` de type ```POST```