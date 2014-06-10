---
layout: post
title: agf-release-test - Ajout balise assertTabCount
tags: [framework-1-81,codjo-release-test,hot-topics]
---
La balise assertTabCount&nbsp;a été ajoutée à la librairie codjo-release-test afin de vérifier le nombre d'onglets dans un TabbedPane.

Par exemple, la balise suivante teste que le JTabbedPane nommé "Nom du JTabbedPane" a 2 onglets.
```
 <assertTabCount name="Nom du JTabbedPane" tabCount="2">
```