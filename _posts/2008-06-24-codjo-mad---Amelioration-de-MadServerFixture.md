---
layout: post
title: agf-mad - Amélioration de MadServerFixture
tags: [codjo-mad,framework-1-50]
---
La classe fixture de test ```MadServerFixture``` à été améliorée : 

* Amélioration du message d'erreur lors de l'appel ```assertSentRequests``` lorsqu'aucune requête n'a été envoyée au serveur.

* Ajout d'une méthode permettant d'obtenir un ```MadConnectionOperations``` (accessible habituellement via ```MadConnectionPlugin.getOperations()```). \\ <u>Exemple</u> : \\ ```java


<u>Exemple</u> : Pour info, il est donc possible facilement de créer un ```Sender``` (accessible habituellement via ```GuiContext.getSender()```). 
```java
