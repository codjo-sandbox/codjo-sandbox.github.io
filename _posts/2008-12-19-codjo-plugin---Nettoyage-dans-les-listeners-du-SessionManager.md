---
layout: post
title: agf-plugin - Nettoyage dans les listeners du SessionManager
tags: [framework-1-76,codjo-plugin]
---
Durant la phase de ```start()``` de ```ApplicationCore```, le ```LdapSecurityService``` enregistre des listeners dans le ```SessionManager```. Par contre, ces listeners n'étaient pas retirés de la liste durant la phase de ```stop()```.

A présent, le ```SessionManager``` supprime bien les listeners durant la phase de ```stop()``` via l'implémentation de l'interface ```Startable``` de pico.