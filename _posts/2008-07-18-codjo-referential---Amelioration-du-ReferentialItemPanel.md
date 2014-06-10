---
layout: post
title: agf-referential - Amélioration du ReferentialItemPanel
tags: [framework-1-53,codjo-referential]
---
Un mécanisme permettant de modifier l'apparence du composant ```ReferentialItemPanel``` a été ajouté. Il est maintenant possible de modifier par exemple le composant graphique représentant un champ.

<u>Exemple</u> : Utilisation du ```PopupDateField``` pour représenter le champ date ```myDate```.
```java
itemPanel.buildPanel(fields, new ReferentialItemPanel.GuiCustomizer() {
    public boolean handle(Field field) {
        return "myDate".equals(field.getName);
    }

    public JComponent createGui(Field field) {
        PopupDateField gui = new PopupDateField();
        field.setComponent(gui);
        return gui;
    }

    public void declareField(DetailDataSource dataSource, Field field) {
        dataSource.declare(field.getName(), field.getComponent());
    }
});
```
