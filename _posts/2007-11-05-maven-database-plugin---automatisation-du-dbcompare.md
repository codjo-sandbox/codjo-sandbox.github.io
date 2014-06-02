---
layout: post
title: maven-database-plugin - automatisation du dbcompare
tags: [framework-1-18,maven-database-plugin]
---
La comparaison de la base des données de développement avec celle de production est de nouveau jouée lors du processus d'intégration (```\-Dprocess=integration```).

Pour activer la comparaison il suffit d'ajouter la propriété suivante dans le pom.xml racine de votre application avec comme valeur le tag subversion de la version en production (ou recette) :
```xml
<properties>
   ....
   <versionInProduction>gabi-3.01.00.00-c</versionInProduction>
</properties>
```
Pour lancer <u>manuellement</u> la comparaison sur GABI:
```
project gabi
mvn install
cd gabi-sql
mvn database:compare-from-prod -DdatabaseType=sybase -Dmaven.database.versionInProduction=gabi-3.01.00.00-c
```\\ Si le paramètre "```maven.database.versionInProduction```" est manquant, la comparaison se jouera avec le tag défini dans le pom applicatif ("```versionInProduction```").