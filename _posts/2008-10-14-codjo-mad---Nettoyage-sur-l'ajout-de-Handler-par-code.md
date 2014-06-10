---
layout: post
title: agf-mad - Nettoyage sur l'ajout de Handler par code
tags: [framework-1-66,codjo-mad]
---
La méthode ```addHandlerCommand(class, Object)``` de la configuration du plugin serveur de codjo-mad a été supprimée car non nécessaire. En effet il existe un mécanisme disponible via les containers pico (soit celui se trouvant dans le socle, soit celui utilisé par une session).

<u>Avant</u>
```java
madServerPlugin.getConfiguration().addHandlerCommand(GetResultCommand.class, manager)
```

<u>Après</u>
* Cas ou l'instance est partagée par toutes les sessions
```java
applicationCore.addGlobalComponent(manager);
madServerPlugin.getConfiguration().addHandlerCommand(GetResultCommand.class)
```
* Cas ou l'instance est partagée seulement dans une session
```java
madServerPlugin.getConfiguration().addSessionComponent(Manager.class);
madServerPlugin.getConfiguration().addHandlerCommand(GetResultCommand.class)
```
