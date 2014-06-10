---
layout: post
title: agf-referential - Modification de la classe ReferentialDetailWindowBuilder
tags: [codjo-referential,framework-1-52]
---
Modification de la classe ```ReferentialDetailWindowBuilder```
En effet, celle-ci ne gère plus, pour son implémentation ou pour ses constructeurs,  un objet ```Map<String, Field>``` mais un objet ```Referential```

Par exemple
```java
ReferentialDetailWindowBuilder(FatherContainer fatherContainer,
                                   String frameTitle,
                                   Referential referential)
```
