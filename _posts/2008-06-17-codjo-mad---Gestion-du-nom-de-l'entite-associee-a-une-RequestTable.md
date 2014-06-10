---
layout: post
title: agf-mad - Gestion du nom de l'entité associée à une RequestTable
tags: [codjo-mad,framework-1-49]
---
Lors du chargement de la préférence de la ```RequestTable```, l'```entityName``` associé au ```DataSource``` est mis à jour (à partir de la préférence) seulement s'il n'a pas déjà été renseigné.