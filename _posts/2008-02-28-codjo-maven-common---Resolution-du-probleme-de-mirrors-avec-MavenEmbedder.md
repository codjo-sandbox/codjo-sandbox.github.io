---
layout: post
title: agf-maven-common - Résolution du problème de mirrors avec MavenEmbedder
tags: [codjo-maven-common,framework-1-33]
---
```MavenEmbedder``` ne prend pas en compte les miroirs définis dans le ```settings.xml```.
```MavenCommand``` a été modifié afin d'utiliser ```CustomizedMavenEmbedder```, un embedder maison qui règle le problème. Ce patch règle notamment le problème de téléchargement d'easymock pour **CAPRI**.

### Rappel

Exemple d'utilisation de MavenCommand :
```java
MavenCommand command = new MavenCommand();
MavenProject project = ...;
Log log = ...;

...

mavenCommand.execute(new String[[]] {"clean", "install"}, project, log);
```