---
layout: post
title: agf-mad - Ajout d'un accesseur dans RequestToolBar
tags: [framework-1-56,codjo-mad]
---
Ajout de l'accesseur retournant une action en fonction de la classe.
```
    public Action getAction(Class actionClass) {
        return allActions.get(actionClass);
    }
```