---
layout: post
title: maven-agf-plugin - Génération de la liste des dépendances à stabiliser
tags: [framework-1-86,maven-codjo-plugin]
---
Lors de la stabilisation, le goal maven ```agf:switch-to-release``` génère un fichier contenant la liste des dépendances à stabiliser.
Par défaut le fichier est généré dans le répertoire temporaire du profil utilisateur sous le nom de ```stabilisationBuildList.txt``` mais il peut être configuré avec l'argument : ```stabilisationFileName```.

Exemple : 
```xml
mvn agf:switch-to-release -DstabilisationFileName=c:\dev\user\temp\monFichier.txt
```