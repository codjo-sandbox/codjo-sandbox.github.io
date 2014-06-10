---
layout: post
title: agf-mad - Gestion du timeout à partir du MadConnectionPlugin
tags: [codjo-mad,framework-1-19]
---
Le plugin ```MadConnectionPlugin``` gère les timeout lors de la communication avec le serveur. Le timeout est configurable globalement ou lors de l'envoie d'une requête spécifique.

<u>Exemple</u> dans Scop pour configurer globalement le timeout il suffit d'utiliser la configuration du plugin ```MadConnectionPlugin```,  :
```java
public class ScopGuiPlugin extends AbstractGuiPlugin {
  public ScopGuiPlugin(MadConnectionPlugin connectionPlugin) {
     // Configuration du timeout global a 60 secondes
     connectionPlugin.getConfiguration().setTimeout(60000);
     ....
  }
 ....
}
```

<u>Exemple</u> pour envoyer une requête avec un timeout spécifique :
```java
// Envoie d'une requête avec un timeout de 2 minutes
connectionPlugin.getOperations().sendRequest(lengthyRequest, 120000 );
```

