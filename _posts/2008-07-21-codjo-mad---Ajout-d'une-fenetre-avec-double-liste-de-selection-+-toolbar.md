---
layout: post
title: agf-mad - Ajout d'une fenêtre avec double liste de sélection + toolbar
tags: [codjo-mad,framework-1-53]
---
Ajout de la classe ```SelectionWindow``` rassemblant un composant ```SelectionGui``` et un ```ButtonPanel```.

Constructeurs:

```
public class SelectionWindow extends JInternalFrame {
...
    public SelectionWindow(String title,
                           RequestTable fromTable, RequestTable toTable,
                           String labelFrom, String labelTo,
                           String borderTitle,
                           GuiContext guiContext,
                           JoinKeys joinKeys,
                           JInternalFrame parentFrame)
...

    public SelectionWindow(String title,
                           RequestTable fromTable, RequestTable toTable,
                           String labelFrom, String labelTo,
                           String borderTitle,
                           GuiContext guiContext,
                           RowFiller rowFiller,
                           JoinKeys joinKeys,
                           JInternalFrame parentFrame)
...
```

Les tables ```fromTable``` et ```toTable``` doivent être préalablement initialisées avec leur préférence et éventuellement avec les sélecteurs.
