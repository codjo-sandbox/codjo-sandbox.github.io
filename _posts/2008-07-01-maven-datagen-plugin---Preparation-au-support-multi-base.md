---
layout: post
title: maven-datagen-plugin - Préparation au support multi-base
tags: [maven-datagen-plugin,framework-1-49]
---
Ajout de l'attribut ```databaseType``` permettant de switcher d'une base à l'autre (par défaut le type est sybase).

<u>Exemple</u> Configuration du plugin pour une base oracle.
```xml
<plugin>
    <groupId>com.agf.maven.mojo</groupId>
    <artifactId>maven-datagen-plugin</artifactId>
    <configuration>
        <databaseType>oracle</databaseType>
    </configuration>
</plugin>
```

<u>Exemple</u> Bascule à chaud vers une base oracle.
```
> project smart
> mvn clean install -DdatabaseType=oracle 
```

{info}
Cette modification est temporaire en attendant le refactoring majeur de juillet portant sur le support multi-base dans le framework.
{info}
