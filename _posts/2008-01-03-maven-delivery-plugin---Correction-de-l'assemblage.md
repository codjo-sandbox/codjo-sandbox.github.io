---
layout: post
title: maven-delivery-plugin - Correction de l'assemblage
tags: [maven-delivery-plugin,framework-1-25,hot-topics]
---
Suite à l'évolution du plugin assemblage différents bugs ont été levés et corrigés :

Nottament la dépendance vers la librairie ```{**}jconnect{**```} était récupérée transitivement via du code de test (```codjo-test```). Il faut donc maintenant la déclarer explicitement dans les modules accédants à la base :
```xml
<dependency>
    <groupId>com.sybase.jdbc</groupId>
    <artifactId>jconnect</artifactId>
</dependency>
```