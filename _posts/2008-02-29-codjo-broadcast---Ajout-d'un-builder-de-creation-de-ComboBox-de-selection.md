---
layout: post
title: agf-broadcast - Ajout d'un builder de création de ComboBox de selection
tags: [codjo-broadcast,framework-1-33]
---
Ajout d'un builder facilitant la création de la ```JComboBox``` permettant de choisir un ```Selector```.

<u>Exemple</u> : tiré de Mint
```java
public class FundPriceGuiPreference extends AbstractGuiPreference {
  ...
  public JComboBox buildSelectionComboBox() throws RequestException {
      return createComboBox(usingBuilder()
            .withSelector("1", "Selection Internet")
            .withSelector("2", "Selection SG"));
  }
...
}
```
