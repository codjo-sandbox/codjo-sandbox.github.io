---
layout: post
title: agf-mad - Correction ouverture fichier Excel
tags: [codjo-mad,framework-1-45]
---
L'implémentation permettant l'ouverture d'un fichier Excel ne fonctionne pas correctement sur toutes les machines (problème environnement Windows sans doute). 

La classe **WindowsHelper** a été corrigée pour résoudre le problème. Elle s'appuie sur la commande suivante :
```
String executableName = "rundll32.exe url.dll,FileProtocolHandler";
Runtime.getRuntime().exec(executableName 
                          + " " 
                          + file.getAbsolutePath());
```

Si vous avez besoin d'une telle fonctionnalité dans votre code de production, le passage par **WindowsHelper** est vivement conseillé.