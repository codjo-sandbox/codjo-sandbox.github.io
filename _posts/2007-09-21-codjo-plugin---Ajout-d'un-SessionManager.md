---
layout: post
title: agf-plugin - Ajout d'un SessionManager
tags: [codjo-plugin,framework-1-13]
---
Ajout de la classe ```SessionManager``` permettant de gérer les sessions utilisateurs. 

<u>Caractéristiques :</u>
* Grâce au ```SessionManager``` il est possible, via un listener, d'être notifié lorsque un utilisateur se connecte (ou se déconnecte) du système.
* Le ```SessionManager``` est multi-thread safe. 
* Ce gestionnaire est accessible par injection de dépendance dans tous les socles (```AgentServer```, ```BatchClient```, etc.). 
* Les plugins implémentant l'interface ```SessionListener``` seront automatiquement déclaré dans le ```SessionManager```.


