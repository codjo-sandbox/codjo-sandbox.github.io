---
layout: post
title: agf-segmentation - Ajout script segmentation.ksh
tags: [framework-1-11,codjo-segmentation]
---
Pour pouvoir le livrer, il faut ajouter les lignes suivantes dans la pom.xml du module batch de l'application : 

```
<build>
        <plugins>
            <plugin>
                <groupId>com.agf.maven.mojo</groupId>
                <artifactId>maven-delivery-plugin</artifactId>
                <configuration>
                    <descriptorId>batch</descriptorId>
                    <includes>
                        <include>
                            <groupId>com.agf.segmentation</groupId>
                            <artifactId>codjo-segmentation-batch</artifactId>
                            <classifier>segmentation</classifier>
                            <type>ksh</type>
                            <output>segmentation.ksh</output>
                        </include>
                    </includes>
                </configuration>
            </plugin>
        </plugins>
    </build>
```