---
layout: post
title: agf-confluence - Modification méthode updatePage(Page page)
tags: [codjo-confluence,framework-1-43]
---
La méthode ```updatePage``` de ```ConfluenceOperations``` renvoie maintenant la page une fois mise à jour dans Confluence. Ceci permet par exemple de récupérer l'id de la page si elle a été créée :

Nouvelle signature :
```
    Page updatePage(Page page) throws ConfluenceException;
```