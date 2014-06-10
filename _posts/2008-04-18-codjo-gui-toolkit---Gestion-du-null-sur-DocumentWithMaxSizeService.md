---
layout: post
title: agf-gui-toolkit - Gestion du null sur DocumentWithMaxSizeService
tags: [codjo-gui-toolkit,framework-1-40]
---
Correction sur DocumentWithMaxSizeService.
La gestion du null sur la chaine de caractères n'était pas faite sur la méthode suivante :
```
public void insertString(int offset, String str, AttributeSet attributeSet)
```