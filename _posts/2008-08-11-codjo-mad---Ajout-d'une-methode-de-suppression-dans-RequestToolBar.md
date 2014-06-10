---
layout: post
title: agf-mad - Ajout d'une méthode de suppression dans RequestToolBar
tags: [framework-1-56,codjo-mad]
---
Ajout dans la classe RequestToolBar, d'une méthode de suppression d'une action en fonction de sa clé, c'est à dire sa classe.

```
    public void removeAction(Class actionClass) {
        Action action = getAction(actionClass);
        if (action == null) {
            return;
        }
        allActions.remove(actionClass);
        removeActionFromPopupMenu(action);
        removeActionFromToolbar(action);
    }

```