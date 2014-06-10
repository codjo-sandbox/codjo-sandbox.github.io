---
layout: post
title: maven-agf-plugin - RollbackSnapshot goal added
tags: [framework-2-25,maven-codjo-plugin]
---
<u>Context</u>
Rollbacking the switch to snapshot of a lib, plugin... was not easy and source of error.
An automatic way of doing it was desirable.

<u>Description</u>
A goal to remove the snapshot and restore the last release version of the artifacts has been implemented.

see. http://wp-confluence/confluence/display/framework/maven-codjo-plugin

<u>Example</u>
```
mvn codjo:rollback-snapshot -Dlib=mad
```
It produces the following traces:
```
[[INFO]] Les fichiers du super-pom ont ete correctement mis a jour.
[[INFO]] Etapes suivantes :
[[INFO]]
[[INFO]] Pour un rollback local - Installation locale du super-pom :
[[INFO]]
[[INFO]]          mvn clean install
[[INFO]]
[[INFO]] Pour un rollback global - Depoiement de la version SNAPSHOT du super-pom :
[[INFO]]
[[INFO]] 1 - Deploiement du super-pom :
[[INFO]]
[[INFO]]          super-pom
[[INFO]]          mvn clean deploy
[[INFO]]
[[INFO]] 2 - Commit des modifications :
[[INFO]]
[[INFO]]          git add .
[[INFO]]          git commit -m "Switch library mad from SNAPSHOT version to last stable version"
[[INFO]]          push
[[INFO]]
[[INFO]]
[[INFO]] 3 - Suppression manuelle de l'artefact en snapshot sur Z :
[[INFO]]
[[INFO]] 4 - Suppression du projet forke dans github :
[[INFO]]      Aller a l'url: https://github.com/codjo-sandbox/codjo-mad/admin
[[INFO]]
```