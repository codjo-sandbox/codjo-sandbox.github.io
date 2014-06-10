---
layout: post
title: agf-mad - Connaitre à l'exécution sur quel environnement on est connecté
tags: [framework-1-16,codjo-mad]
---
La property système "user.environment" contient maintenant la valeur  sélectionnée dans la comboBox de choix du serveur lors du login dans une application. (Pour mémo, les valeurs dans la combo sont définies dans application.properties).
```
          // exemple ... 
          if ("Production".equals(System.getProperty("user.environment"))) {
            // ... mettre la couleur du desktop en rouge fluo
          }
```\\