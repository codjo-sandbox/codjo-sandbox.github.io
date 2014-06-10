---
layout: post
title: agf-pom - Activation des profils base de données
tags: [framework-1-54,codjo-pom]
---
Le paramétrage et l'activation du plugin ```maven-profile-plugin``` ont été mis en place.
Par défaut, les applications et les lib chargent le profil Sybase.
Il est possible de spécifier un autre profil que celui par défaut en spécifiant _-DdatabaseType=xxx_ à la ligne de commande ```maven``` (xxx pouvant être ```sybase```, ```mysql```, ```oracle``` et ```hsqldb```).

<u>Exemple</u> : install en ```mysql```
```
mvn clean install -DdatabaseType=mysql
```