---
layout: post
title: agf-webservices - Ajout d'un SoapRequestSender pour envoyer des requêtes de type SOAP vers un serveur Web
tags: [framework-1-64,codjo-webservices]
---
Une classe de type "main" ```SoapRequestSender``` a été créée afin de pouvoir envoyer une requête de type SOAP contenue dans un fichier vers un serveur Web. Le résultat est stocké dans un fichier passé en argument.

**{<u>}Usage{</u>}**
```
SoapRequestSender URL REQUEST-FILE RESPONSE-FILE
```