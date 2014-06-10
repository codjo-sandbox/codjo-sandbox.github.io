---
layout: post
title: agf-referential - Amélioration de la configuration du plugin GUI
tags: [framework-1-53,codjo-referential]
---
Le ```ListGuiCustomizer``` permettant de modifier les IHM de référentiel est maintenant instancié lors de l'ouverture de l'écran des référentiels. Cela permet d'utiliser un ```ListGuiCustomizer``` comme un système de cache.

La configuration se fait donc en précisant une classe et non plus une instance. 

<u>Exemple</u> 
```java
referentialGuiPlugin.getConfiguration().setListGuiCustomizer(AddLabelCustomizer.class);
```

 