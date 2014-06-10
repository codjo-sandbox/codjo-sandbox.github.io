---
layout: post
title: agf-mad - Optimisation des échanges client-serveur
tags: [codjo-mad,framework-1-4]
---
Les résultats des requêtes envoyées au serveur MAD sont à présent zippés.
Utilisation des ```AclMessage.setContent``` ou ```AclMessage.setByteSequenceContent``` à la place du ```AclMessage.setContentObject``` pour optimisation.