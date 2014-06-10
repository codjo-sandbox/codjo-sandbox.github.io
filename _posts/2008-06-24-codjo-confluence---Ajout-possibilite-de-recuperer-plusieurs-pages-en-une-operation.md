---
layout: post
title: agf-confluence - Ajout possibilité de récupérer plusieurs pages en une opération
tags: [codjo-confluence,framework-1-49]
---
Ajout d'une méthode ```getPages``` sur ```ConfluenceOperations``` qui permet de récupérer plusieurs pages en une seule opération. Ceci permet d'éviter les temps de connexion et de déconnexion.

```
public List<Page> getPages(List<String> pageIds) throws ConfluenceException;
```


Exemple :
```
List<String> pageIds = Arrays.asList("page1", "page2", "page3");
List<Page> pages = operations.getPages(pageIds);
```