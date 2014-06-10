---
layout: post
title: maven-test-release-plugin - Temps d'attente après démarrage local du serveur
tags: [maven-test-release-plugin,framework-1-26]
---
Ajout de la propriété ```sleepAfterLocalStart``` permettant de configurer un temps d'attente du serveur après son démarrage avant l'exécution des tests release.

Par défaut, la valeur de ```sleepAfterLocalStart``` est égale à 0.

<u>Exemple 1</u> Pour configurer 5 secondes d'attente, il faut modifier le fichier pom.xml du module release-test comme suit: 

```

<plugin>
     <groupId>com.agf.maven.mojo</groupId>
     <artifactId>maven-test-release-plugin</artifactId>
     <configuration>
          <sleepAfterLocalStart>5</sleepAfterLocalStart>
           ...
     </configuration>
</plugin>

```

<u>Exemple 2</u> En ligne de commande :

```
mvn -DsleepAfterLocalStart=5 install -Dprocess=integration
```
