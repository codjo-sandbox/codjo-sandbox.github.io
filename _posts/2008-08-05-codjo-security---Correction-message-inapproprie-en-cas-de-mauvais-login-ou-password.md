---
layout: post
title: agf-security - Correction message inapproprié en cas de mauvais login ou password
tags: [codjo-security,framework-1-55]
---
Lors de la phase de connexion via ```Mad```, en cas de mauvais login/password, le message d'erreur remonté à l'utilisateur était incorrect ("Le serveur ne semble pas répondre..." au lieu de "Compte ou mot de passe incorrect"). 

Ceci était dû au fait que lors d'une exception ```BadLoginException``` remontée par le serveur, le client ne parvenait pas à décoder le message Jade contenant l'exception. Celle-ci étant en effet contenue dans le module ```server``` de ```codjo-security```, le client n'avait pas la dépendance requise. 

La classe ```BadLoginException``` a donc été déplacée dans le module ```common``` de ```codjo-security```.