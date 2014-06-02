---
layout: post
title: maven-agf-plugin - Création du goal idea-glue
tags: [framework-1-99,maven-codjo-plugin,hot-topics]
---
Le goal ```idea-glue``` a été créé. Il permet de lier au sein d'un même projet ```IntelliJ``` des applications, des librairies ou des plugins.
La commande ```idea.cmd``` a été mise à jour afin d'utiliser ce goal.

<u>Exemples d'utilisation d'```idea.cmd```</u>
```

C:\dev\projects\sam> idea -Dlib=datagen -Dplugin=datagen

..  Lie sam, lib datagen et plugin datagen dans un projet sam-glue.ipr

C:\dev\projects\sam> idea -Dappli=red -Dlib=agent,mad

..  Lie sam, red, agent et mad dans un projet sam-glue.ipr

```