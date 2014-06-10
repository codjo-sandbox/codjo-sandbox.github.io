---
layout: post
title: agf-mad - Remplacement des actions de la RequestToolBar
tags: [framework-1-90,codjo-mad]
---
Précédemment, le remplacement de certaines actions (```FindAction``` notamment) posait des problèmes.

Par exemple, après avoir remplacé la ```FindAction```, il n'était plus possible d'utiliser les méthodes ```RequestToolBar.setSqlRequetorMandatoryClause()``` et ```RequestToolBar.setSqlRequetorOrderClause()```.

Cela a été corrigé.