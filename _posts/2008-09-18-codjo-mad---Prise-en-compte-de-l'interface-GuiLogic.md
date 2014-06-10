---
layout: post
title: agf-mad - Prise en compte de l'interface GuiLogic
tags: [codjo-mad,framework-1-62]
---
Prise en compte dans les "Logic" de codjo-mad de l'interface ```GuiLogic```. Cette interface est pratique pour guider le développeur.

<u>Exemple</u> le ```ButtonPanelLogic```
```java
public class ButtonPanelLogic implements GuiLogic<ButtonPanelGui> {
   ...
   public ButtonPanelGui getGui() {...}
   ...
}
```
