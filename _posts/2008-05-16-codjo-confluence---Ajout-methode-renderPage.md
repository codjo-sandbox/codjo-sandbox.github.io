---
layout: post
title: agf-confluence - Ajout méthode renderPage
tags: [codjo-confluence,framework-1-44]
---
Ajout de la méthode ```renderPage``` à ```ConfluenceOperations``` permettant de déclencher le moteur de rendu de confluence.

```
String renderPage(String spaceKey, String pageId, String content) throws ConfluenceException;
```
si ```content``` est une chaîne vide, la méthode renvoie le résultat du rendu du contenu de la page. Sinon, la méthode renvoie le rendu qu'on obtiendrait si le contenu de la page était ```content```.

Exemple :
```
String html = operations.renderPage("mySpace", "1234", "");
```