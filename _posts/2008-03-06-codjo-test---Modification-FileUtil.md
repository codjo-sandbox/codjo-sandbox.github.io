---
layout: post
title: agf-test - Modification FileUtil
tags: [codjo-test,framework-1-34]
---
Ajout de la méthode ```loadContent(URL)``` sur la classe ```FileUtil```. Cette méthode permet de charger le contenu d'un fichier à partir d'une URL.

<u>Exemple</u> : Chargement d'une ressource et d'une page HTML.
```java
String expected = FileUtil.loadContent(getClass().getResource("google-main.txt"));
String actual = FileUtil.loadContent(new URL("http://google.com"));
```
