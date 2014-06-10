---
layout: post
title: maven-agf-plugin - Improve help goal
tags: [framework-2-32,maven-codjo-plugin,hot-topics]
---
<u>Context</u>
The codjo help on the super-pom was inaccurate (same as an application).

<u>Description</u>
The goal ```codjo:help``` has been updated to give the goals that can be used with the super-pom and an application.

<u>Example</u>
_Super-pom_
```c:codjo-pom>mvn codjo:help
[[INFO] [codjo:help]]
[[INFO]]       type Projet super-pom
[[INFO]]
...
Commandes Disponibles
---------------------
    mvn [[deploy|install|clean]]
        Deploiement, installation ou nettoyage du projet

    idea [[clean|help] [-Dappli=...] [-Dlib=...] [-Dplugin=...]]
        Creation du projet IntelliJ Idea

    mvn codjo:switch-to-snapshot [[-Dlib=...|-Dplugin=...]]
        Ouverture de chantier dans le super-pom

    mvn codjo:rollback-snapshot [[-Dlib=...|-Dplugin=...]]
        Annulation d'une ouverture de chantier dans le super-pom

Options
-------

    -Dlib=...
        Librairie concernee. (ex. -Dlib=workflow)

    -Dplugin=...
        Plugin concerne. (ex. -Dplugin=codjo)
```
_Application_
```
c:codjo-sample>mvn codjo:help
[[INFO] [codjo:help]]
[[INFO]]       type Projet Racine
[[INFO]]
...
Commandes Disponibles
---------------------
    mvn [[install|clean] [options]]
        Installation ou nettoyage du projet

    idea [[clean|help] [-Dappli=...] [-Dlib=...] [-Dplugin=...]]
        Creation du projet IntelliJ Idea

        -Dappli=...
            Applications a lier au projet. (ex. -Dappli=sam)

        -Dlib=...
            Librairies a lier au projet. (ex. -Dlib=workflow,imports)

        -Dplugin=...
            Plugins a lier au projet. (ex. -Dplugin=codjo,datagen)

    mvn codjo:switch-to-parent-release
        Bascule sur la derniere version stable du super-pom

    mvn codjo:switch-to-parent-snapshot
        Bascule sur la version SNAPSHOT du super-pom

Options
-------

    -Dprocess=integration
        Lancement du process d'integration

    -Ddatabase=integration
        Utilisation de la BD integration

    -Dserver=integration
        Utilisation du serveur d'integration

    -Dcoverage=true
        Active la couverture de code par les test-release
```

see: http://wp-confluence/confluence/display/framework/maven-codjo-plugin
