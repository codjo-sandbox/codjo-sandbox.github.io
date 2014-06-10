---
layout: post
title: maven-datagen-plugin - Lancement de la génération dans une VM séparée
tags: [maven-datagen-plugin,framework-1-5]
---
La génération se fait dorénavant dans une VM séparée.

On peut passer des paramètres à cette VM à l'aide d'une nouvelle propriété "vmArguments" à spécifier dans la configuration du plugin. Exemple :
```
<plugin>
    <groupId>com.agf.maven.mojo</groupId>
    <artifactId>maven-datagen-plugin</artifactId>
    <configuration>
        <includes>
            ....
        </includes>
        <vmArguments>-Xms256m -Xmx512m -XX:MaxPermSize=256m</vmArguments>
    </configuration>
</plugin>
```
Cette propriété est facultative, par défaut les arguments passés sont ceux décrit dans l'exemple.