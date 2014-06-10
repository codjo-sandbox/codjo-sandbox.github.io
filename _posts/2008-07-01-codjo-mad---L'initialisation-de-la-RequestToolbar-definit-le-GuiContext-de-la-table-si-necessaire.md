---
layout: post
title: agf-mad - L'initialisation de la RequestToolbar définit le GuiContext de la table si nécessaire
tags: [codjo-mad,framework-1-50]
---
Maintenant l'initialisation de la ```RequestToolbar``` (i.e. l'appel de la méthode ```init(GuiContext,RequestToolbar)```) définit le ```GuiContext``` de la table si il n'est pas déjà défini.

Voici le code en question : 
```java
if (table.getDataSource() != null && table.getDataSource().getGuiContext() == null) {
  table.getDataSource().setGuiContext(guiContexte);
}
```
