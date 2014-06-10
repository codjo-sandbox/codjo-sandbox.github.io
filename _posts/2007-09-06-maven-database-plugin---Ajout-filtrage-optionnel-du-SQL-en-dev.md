---
layout: post
title: maven-database-plugin - Ajout filtrage optionnel du SQL en dev
tags: [maven-database-plugin,framework-1-11]
---
Il est maintenant possible de filter le SQL situé dans /src/main/sql avant exécution en dev à l'aide d'un nouveau paramètre de configuration dans le pom.xml du module SQL :
```
<plugins>
    <plugin>
        <groupId>com.agf.maven.mojo</groupId>
        <artifactId>maven-database-plugin</artifactId>
        <configuration>
            <filters>
                <filter>
                    <token>A_REMPLACER</token>
                    <value>NOUVELLE_VALEUR</value>
                </filter>
            </filters>
            ...
        </configuration>
    </plugin>
    ...
</plugins>
```

Ce filtrage n'est appliqué que pour le développement, lors de la livraison, les fichiers originaux non filtrés sont packagés.