---
layout: post
title: agf-referential - Creation d'une classe DefaultGuiCustomizer
tags: [framework-1-90,codjo-referential]
---
Afin de pouvoir utiliser, dans un autre projet, la création par défaut des composants graphiques à partir d'objets ```Field```, une classe ```DefaultGuiCustomizer``` a été extraite de ```ReferentialItemPanel```.

Ainsi, il est possible de créer un autre ```GuiCustomizer``` utilisant par aggrégation le comportement du ```DefaultGuiCustomizer```.