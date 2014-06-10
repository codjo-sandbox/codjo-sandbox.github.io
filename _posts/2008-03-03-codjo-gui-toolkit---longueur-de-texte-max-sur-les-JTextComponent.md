---
layout: post
title: agf-gui-toolkit - longueur de texte max sur les JTextComponent
tags: [codjo-gui-toolkit,framework-1-33]
---
Une nouvelle classe, ```DocumentWithMaxSizeService```, a fait son apparition qui permet de fixer la longueur max sur un composant de type ```JTextComponent```.

Exemple :
```java
JTextComponent textComponent = ...;
int maxTextLength = ...;
DocumentWithMaxSizeService.install(textComponent, maxTextLength);
```