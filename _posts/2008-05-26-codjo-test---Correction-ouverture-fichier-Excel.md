---
layout: post
title: agf-test - Correction ouverture fichier Excel
tags: [codjo-test,framework-1-45]
---
Homogénéisation de la méthode d'ouverture d'un fichier Excel.
L'implémentation permettant l'ouverture d'un fichier Excel ne fonctionne pas correctement sur toutes les machines (problème environnement Windows sans doute). 

Pour résoudre le problème, la commande suivante a été utilisée :
```
String executableName = "rundll32.exe url.dll,FileProtocolHandler";
Runtime.getRuntime().exec(executableName <u> " " </u> file.getAbsolutePath());
```

A cause de problèmes de dépendances, la classe **WindowsHelper** dans codjo-mad n'a pas pu être réutilisée mais il est vivement conseillé de réutiliser cette classe d'agf-mad si vous avez le même genre de problématique dans votre code de production.