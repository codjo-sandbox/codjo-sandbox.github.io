---
layout: post
title: agf-referential - Ajout d'un système permettant de modifier les IHM
tags: [codjo-referential,framework-1-51]
---
Ajout d'un système permettant de modifier les IHM de référentiel via l'introduction de la notion de ```ListGuiCustomizer```.

<u>Exemple</u> : Pour ajouter un libellé au dessus de l'affichage en liste
1. Création du customizer
```java
class AddLabelCustomizer implements ListGuiCustomizer {

    public void handleListOpen(Referential referential, ReferentialListGui listGui) {
        listGui.setTopPanel(new PanelWithLabel());
    }


    public void handleListClose(ReferentialListGui listGui) {
        listGui.setTopPanel(null);
    }
}
```
1. Configuration du customizer
```java
referentialGuiPlugin.getConfiguration().setListGuiCustomizer(new AddLabelCustomizer());
```
