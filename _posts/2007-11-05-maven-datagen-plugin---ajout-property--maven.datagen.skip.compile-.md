---
layout: post
title: maven-datagen-plugin - ajout property "maven.datagen.skip.compile"
tags: [framework-1-18,maven-datagen-plugin]
---
Si on positionne cette propriété, la compilation des sources se désactive.

Ex:
```
mvn install -Dmaven.datagen.skip.compile=true
```