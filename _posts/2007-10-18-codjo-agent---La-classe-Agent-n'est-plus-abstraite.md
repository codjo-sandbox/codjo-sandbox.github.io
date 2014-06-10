---
layout: post
title: agf-agent - La classe Agent n'est plus abstraite
tags: [codjo-agent,framework-1-17]
---
La classe ```Agent``` n'est plus une classe abstraite. Un constructeur prenant un ```Behaviour``` en paramètre est ajouté.

Il est donc maintenant possible de créer un agent mono comportemental très simplement:
```java
agentContainer.acceptNewAgent("sylar", new Agent(new KillerBehaviour()).start();
```
