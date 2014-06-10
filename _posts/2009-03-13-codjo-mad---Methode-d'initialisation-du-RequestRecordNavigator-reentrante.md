---
layout: post
title: agf-mad - Méthode d'initialisation du RequestRecordNavigator réentrante
tags: [framework-1-87,codjo-mad]
---
Lors de l'initialisation d'une RequestToolBar,&nbsp;son RequestRecordNavigator est initialisé. Cette initialisation&nbsp;a été faite réentrante&nbsp;en évitant d'enregistrer plusieurs fois les mêmes listeners.

Il devient ainsi possible de&nbsp;redéfinir les préférences d'une RequestTable&nbsp;et de mettre à jour&nbsp;sa RequestToolBar en employant la séquence d'appels suivante :
```
table.setPreference(preference);
getGui().getToolBar().init(guiContext, table);
```