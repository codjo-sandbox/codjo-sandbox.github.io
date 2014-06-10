---
layout: post
title: agf-pom - Ajout de la lib jetty-jsp
tags: [framework-1-54,codjo-pom]
---
La librairie jsp a été ajoutée au super-pom. C'est une librairie permettant de compiler des pages jsp dans jetty. Pour l'utiliser, ajouter ceci dans votre fichier pom.xml :
```
<dependency>
     <groupId>org.mortbay.jetty</groupId>
     <artifactId>jsp-2.1</artifactId>
</dependency>
```