---
layout: post
title: agf-referential - Modification des actions dans la "toolbar"
tags: [framework-1-56,codjo-referential]
---
&nbsp;Ajout d'une méthode permettant de remplacer une action par une autre, dans la "toolbar" de la classe DefaultReferentialListGui.
```
public void replaceToolBarAction(Class<? extends Action> oldActionClassKey, Action newAction) {
        toolBar.removeAction(oldActionClassKey);
        toolBar.add(newAction, RequestToolBar.ACTION_ADD, false);
}
```