---
layout: post
title: agf-segmentation - Ajout du module Batch
tags: [framework-1-9,codjo-segmentation]
---
Le module batch a été ajouté dans le projet afin de déclencher via VTOM le calcul de la segmentation.

Pour configurer les applications avec ce nouveau plugin, il suffit de suivre les instructions suivantes

* Ajouter une dependance vers ```codjo-segmentation-batch``` dans le ```pom.xml``` du module batch
* Ajouter le plugin dans la classe principale du module batch de l'application même. Ex, dans ```roses-batch``` :
```
CommandLineArguments arguments = new CommandLineArguments(args);
BatchClient batch = new BatchClient(arguments);
batch.addPlugin(SegmentationBatchPlugin.class);
batch.start();
batch.executeAndExit();
```

* Afin de pouvoir livrer le ksh, il faut ajouter les lignes suivantes dans la pom.xml du module batch de l'application :
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