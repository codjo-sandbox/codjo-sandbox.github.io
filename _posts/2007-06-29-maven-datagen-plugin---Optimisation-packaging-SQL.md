---
layout: post
title: maven-datagen-plugin - Optimisation packaging SQL
tags: [maven-datagen-plugin,framework-1-4]
---
Une optimisation a été mise en place pour éviter le packaging des scripts SQL lorsque cela ne s'avère pas nécessaire.

Lorsque l'on ne modifie pas Datagen, les scripts SQL ne sont pas regénérés et donc le packaging des scripts SQL ne se refait pas.