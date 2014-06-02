---
layout: post
title: maven-datagen-plugin - Activation et désactivation des générateurs
tags: [framework-1-69,maven-datagen-plugin]
---
Ajout de la possibilité d'activer (et donc de désactiver) un ensemble spécifique de générateur datagen.

Les plugins sont regroupé en 3 domaines techniques : 
* ```JAVA``` : regroupe tous les générateurs produisant du code JAVA (handler, bean, etc.)
* ```SQL``` : regroupe tous les générateurs produisant du code SQL (table, trigger, etc.)
* ```CONFIGURATION``` : regroupe tous les générateurs produisant de la configuration (```structure.xml```, configuration castor, etc.)

<u>Exemple</u> Pour n'activer que les générateur SQL et CONFIGURATION, il faut modifier le ```pom.xml``` du module datagen comme indiqué : 
```xml
<plugin>
  <groupId>com.agf.maven.mojo</groupId>
  <artifactId>maven-datagen-plugin</artifactId>
  <configuration>
      <activatedGeneratorTypes>CONFIGURATION, SQL</activatedGeneratorTypes>                    
      ...
  </configuration>
</plugin>
```
