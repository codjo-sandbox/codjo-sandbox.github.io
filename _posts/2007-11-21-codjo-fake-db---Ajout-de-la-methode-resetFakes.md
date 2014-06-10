---
layout: post
title: agf-fake-db - Ajout de la méthode resetFakes
tags: [framework-1-21,codjo-fake-db]
---
Ajout de la méthode ```resetFakes()``` permettant de vider les piles contenant les requêtes simulées.

<u>Exemple</u>:
```java
FakeDriver.getDriver().resetFakes();
```
