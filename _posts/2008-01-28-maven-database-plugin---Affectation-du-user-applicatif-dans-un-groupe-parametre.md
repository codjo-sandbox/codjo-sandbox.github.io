---
layout: post
title: maven-database-plugin - Affectation du user applicatif dans un groupe paramétré
tags: [framework-1-28,maven-database-plugin]
---
Ajout de la configuration du groupe Sybase du compte applicatif (habituellement ```APP_USER```) :
```
<plugin>
    <groupId>com.agf.maven.mojo</groupId>
    <artifactId>maven-database-plugin</artifactId>
    <configuration>
        <databaseApplicationGroup>Applicatif</databaseApplicationGroup>
    </configuration>
</plugin>
```
Le groupe par défaut est le groupe ```Utilisateur```.