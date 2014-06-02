---
layout: post
title: maven-database-plugin - Livraison de procédures dans une librairie
tags: [maven-database-plugin,framework-1-10]
---
Il est maintenant possible de livrer des procédures avec une librairie. Auparavant seules les procédures de l'application étaient exécutées. Il suffit d'ajouter dans l'artifact sql un fichier procedure-order.sql à la racine de l'arborescence qui contient la liste des procédures à exécuter dans l'ordre souhaité. (Même principe que pour les fichiers procedure-order.sql présents dans les applis). Exemple :
```
lib-sql.jar
   \__ table
   \__ ...
   \__ procedure
      \__ sp1.sql
      \__ sp2.sql
   \__ procedure-order.txt
```
Contenu de procedure-order.txt :
```
procedure\sp1.sql
procedure\sp2.sql
```