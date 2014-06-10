---
layout: post
title: agf-mad - Bug sur ListDataSource
tags: [codjo-mad,framework-1-90]
---
Lorsque le nombre de lignes total est multiple de ```ListDataSource.PAGE_SIZE``` et que l'on se situe à la dernière page, la méthode ```hasNextPage()``` renvoyait ```true``` alors qu'elle doit renvoyer ```false```. Ce bug est maintenant corrigé.