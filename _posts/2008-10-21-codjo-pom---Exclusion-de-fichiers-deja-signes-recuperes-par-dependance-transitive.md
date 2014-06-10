---
layout: post
title: agf-pom - Exclusion de fichiers déjà signés récupérés par dépendance transitive
tags: [framework-1-67,codjo-pom]
---
Les librairies PDFBox et IText tirent par dépendance transitives 2 jars non nécéssaires (cryptographie) et déjà signés.
```
         <dependency>
                <groupId>com.lowagie</groupId>
                <artifactId>itext</artifactId>
                <version>2.1.2</version>
                <exclusions>
                    <exclusion>
                        <groupId>bouncycastle</groupId>
                        <artifactId>bcmail-jdk14</artifactId>
                    </exclusion>
                    <exclusion>
                        <groupId>bouncycastle</groupId>
                        <artifactId>bcprov-jdk14</artifactId>
                    </exclusion>
                </exclusions>
            </dependency>
            <dependency>
                <groupId>pdfbox</groupId>
                <artifactId>pdfbox</artifactId>
                <version>0.7.3</version>
                <exclusions>
                    <exclusion>
                        <groupId>bouncycastle</groupId>
                        <artifactId>bcmail-jdk14</artifactId>
                    </exclusion>
                    <exclusion>
                        <groupId>bouncycastle</groupId>
                        <artifactId>bcprov-jdk14</artifactId>
                    </exclusion>
                </exclusions>
            </dependency>
```

Pour rappel, la signature des Jars empêche la livraison des applications puisque les jar livrés sont signés par DELRECO. Les Jars ont donc aussi été supprimés du répository distant.