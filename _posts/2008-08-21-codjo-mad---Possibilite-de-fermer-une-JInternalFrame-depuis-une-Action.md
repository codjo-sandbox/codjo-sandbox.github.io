---
layout: post
title: agf-mad - Possibilité de fermer une JInternalFrame depuis une Action
tags: [framework-1-57,codjo-mad]
---
Ajout de la méthode ```closeFrame()``` dans la classe abstraite ```AbstractAction``` supervisant une ```JInternalFrame``` qui permet aux classes filles de fermer leur fenêtre.

par exemple : 
```
public class MyAction extends AbstractAction {

    public MyAction (GuiContext guiContext) {
        super(guiContext, "MyAction", "MyAction");
    }


    @Override
    protected JInternalFrame buildFrame(GuiContext ctxt) throws Exception {
        return new MyLogic().getGui();
    }


    public void closeMyFrame() {
        super.closeFrame(); //closeFrame est protected dans AbstractAction
    }
```