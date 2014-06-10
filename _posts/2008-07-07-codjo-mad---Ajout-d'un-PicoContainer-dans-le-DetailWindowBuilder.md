---
layout: post
title: agf-mad - Ajout d'un PicoContainer dans le DetailWindowBuilder
tags: [codjo-mad,framework-1-51]
---
Afin d'ajouter plus de flexibilité, les écrans détails sont maintenant construits avec un ```PicoContainer```. 

Cela permet :
1. D'être plus libre concernant l'ordre des arguments dans le constructeur. 
1. De pouvoir ajouter des arguments facilement en modifiant le ```DetailWindowBuilder```

<u>Exemple</u> de customization du ```DetailWindowBuilder```.
```java
public class MyDetailWindowBuilder extends DetailWindowBuilder {
    protected void fillPicoContainer(MutablePicoContainer pico, DetailDataSource ds, Preference dsPref) {
    super.fillPicoContainer(pico, ds, dsPref);
    pico.registerComponentInstance(MyArgument.class, myArgument);
  }
}
```

