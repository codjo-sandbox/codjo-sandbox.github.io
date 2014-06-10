---
layout: post
title: agf-gui-toolkit - Limitation du nombre de caractères saisis dans une table
tags: [codjo-gui-toolkit,framework-1-114]
---
Il est maintenant possible de limiter le nombre de caractères saisis dans une cellule d'une ```JTable```, en utilisant le constructeur de la classe ```TextFieldEditor``` suivant:
```
public TextFieldEditor(int sizeLimit);
```