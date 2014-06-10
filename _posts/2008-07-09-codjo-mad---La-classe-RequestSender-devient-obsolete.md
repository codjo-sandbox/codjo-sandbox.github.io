---
layout: post
title: agf-mad - La classe RequestSender devient obsolète
tags: [codjo-mad,framework-1-52]
---
La classe ```RequestSender``` devient obsolète. 

Pour rappel, il existe deux méthodes permettant d'envoyer des requêtes au serveur.

1. Utilisation du plugin ```MadConnectionPlugin```
```java
madConnectionPlugin.getOperations().sendRequest(myUpdateRequest);
```
1. Utilisation du ```Sender``` se trouvant sur le ```GuiContext```
```java
guiContext.getSender().sendRequest(myUpdateRequest);
```
