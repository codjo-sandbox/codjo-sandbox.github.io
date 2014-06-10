---
layout: post
title: agf-gui-toolkit - Bug sur maxTextLength
tags: [codjo-gui-toolkit,framework-1-33]
---
Résolution d'un bug sur le ```maxTextLength``` d'un ```TextField``` : on ne peut plus insérer de chaine de caractères dont la taille dépasse celle autorisée.

Rappel d'utilisation :
```java
TextField textField = ...;
int maxTextLength = ...;
testField.setMaxTextLength(maxTextLength);
```