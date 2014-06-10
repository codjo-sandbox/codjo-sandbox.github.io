---
layout: post
title: agf-mad - Méthode de lancement d'Excel
tags: [codjo-mad,framework-1-44,excel]
---
Nous avons modifié la méthode de lancement d'Excel de façon à pouvoir avoir la main sur un instance d'Excel au moment des Test Release.
Au lieu d'appeler
```
Runtime.getRuntime().exec("rundll32.exe url.dll,FileProtocolHandler")
```
nous appelons désormais une méthode statique de codjo-mad :
```
WindowsHelper.openWindowsFile((File)input);
```
Cette méthode se base sur la commande DOS **start** qui ne démarre pas une nouvelle instance d'Excel si une instance existe déjà.
