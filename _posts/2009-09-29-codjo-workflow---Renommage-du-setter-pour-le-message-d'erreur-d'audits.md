---
layout: post
title: agf-workflow - Renommage du setter pour le message d'erreur d'audits
tags: [framework-1-115,codjo-workflow]
---
La méthode ```JobAudit.setError(String)``` a été renommée en ```setErrorMessage(String)``` pour correspondre au getter associé ```getErrorMessage()```.