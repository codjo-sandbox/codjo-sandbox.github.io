---
layout: post
title: agf-mad - Connexion sur différents domaines
tags: [framework-1-104,codjo-mad]
---
Il est maintenant possible pour l'utilisateur de choisir le domaine sur lequel il souhaite s'authentifier.

Afin de répondre rapidement à un besoin **urgent**, il est pour le moment nécessaire de spécifier dans la configuration du client les labels des différents domaines qui seront affichés dans la fenêtre de login.

Il suffit d'ajouter dans le fichier ```application.properties``` :
```
server.ldap.default = Domaine Par Défaut
server.ldap._otherDomain1_ = Autre Domaine
server.ldap.otherDomain2 = Encore un Autre Domaine
```

ou _otherDomain1_ correspond à la propriété défini dans la fichier ```server-config.properties``` (cf [[news sur security|/2009/07/10/codjo-security - Connexion sur différents domaines]])