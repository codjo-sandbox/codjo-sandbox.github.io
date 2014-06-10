---
layout: post
title: agf-tokio - Bug dans la composition d'entités
tags: [framework-1-107,codjo-tokio]
---
Précédemment, si une entité possédant un ```required``` était inclue dans une autre entité, cela générait un ```NullPointerException```.

Cela a été corrigé.