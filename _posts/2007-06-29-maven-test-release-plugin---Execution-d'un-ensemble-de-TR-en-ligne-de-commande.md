---
layout: post
title: maven-test-release-plugin - Exécution d'un ensemble de TR en ligne de commande
tags: [maven-test-release-plugin,framework-1-4]
---
Il est possible de lancer les Tests Release en spécifiant un Test Release spécifique ou un répertoire de Tests Release.
Pour cela, il faut que le serveur soit démarré. Puis en ce plaçant dans le module apli-release-test, il suffit d'exécuter la commande en précisant l'argument **test** correspondant à ce que l'on souhaite exécuter.

```
C:\DEV\projects\mint\mint-release-test>mvn test-release:run
-Dtest=src\main\usecase\AssociationProduitBench\IhmAssociationProduitBench.xml -DdatabaseType=sybase
```

La complétion étant disponible, il est facile de spécifier un chemin vers le TR à exécuter.
