---
layout: post
title: agf-mad - Ajout et positionnement de l'action dans la RequestToolBar
tags: [framework-1-90,codjo-mad]
---
Il est maintenant possible de choisir la position d'une nouvelle action à ajouter à la ```RequestToolBar```.
```java|title=Ajout à gauche d'une action
toolBar.add(myAction, "MyAction", Position.left(RequestToolBar.ACTION_EDIT));
```
\\
```java|title=Ajout à droite d'une action, avec ajout dans la popup
toolBar.add(myAction, "MyAction", Position.right(RequestToolBar.ACTION_EDIT), true);
```
\\
```java|title=Ajout après la dernière action
toolBar.add(myAction, "MyAction", Position.last());
```