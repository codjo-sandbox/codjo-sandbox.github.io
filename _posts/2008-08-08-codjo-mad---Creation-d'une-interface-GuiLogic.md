---
layout: post
title: agf-mad - Création d'une interface GuiLogic
tags: [framework-1-56,codjo-mad]
---
Création d'une interface permettant de définir le contrat devant être rempli par les classes Logic :

```
public interface GuiLogic<T extends Component> {

    public T getGui();
}
```
