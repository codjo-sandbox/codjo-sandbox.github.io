---
layout: post
title: agf-agent - ajout d'un nom sur Behaviour
tags: [framework-1-6,codjo-agent]
---
Ajout des methodes ```setBehaviourName``` et ```getBehaviourName``` permettant de modifier le nom du comportement. Le nom par défaut est celui de la classe. Ce nom apparaît notamment dans les IHM du RMA.

<u>Exemple :</u>

```java
Behaviour behaviour = new BehaviourMock();
assertEquals("BehaviourMock", behaviour.getBehaviourName());
```
