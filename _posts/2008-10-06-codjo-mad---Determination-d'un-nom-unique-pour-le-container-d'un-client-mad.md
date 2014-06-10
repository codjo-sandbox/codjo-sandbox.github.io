---
layout: post
title: agf-mad - Détermination d'un nom unique pour le container d'un client mad
tags: [framework-1-65,codjo-mad]
---
Dans la classe ```MadConnectionPlugin```, la méthode ```IdUtil.createUniqueId(Object anObject)``` de la librairie **codjo-agent** est utilisée afin de déterminer un identifiant unique pour le nom du container et le nom de l'agent "président".

Cela permet de corriger un bug de connexion dans le cas où l'on déployait plusieurs agents "président" dans le même container avec pour conséquence la perte (aléatoire) de certains messages.

Par conséquent, la
[[mise en place d'une nouvelle tentative de connexion dans le cas où le serveur ne répondait pas|/2008/08/05/codjo-mad - Mise en place d'une nouvelle tentative de connexion si le serveur ne répond pas]], devenue inutile, a été supprimée.