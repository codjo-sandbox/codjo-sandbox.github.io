---
layout: post
title: agf-referential - Ajout écran d'administration des familles de référentiels
tags: [framework-1-19,codjo-referential]
---
L'administration des familles se fait dorénavant par l'intermédiaire d'un écran d'administration, avec stockage en base. La configuration par l'intermédiaire de datagen est supprimée.

Nouvelle action à insérer au menu.xml :
```
<menu plugin="com.agf.referential.gui.plugin.ReferentialGuiPlugin" actionId="referentialFamily"/>
```
