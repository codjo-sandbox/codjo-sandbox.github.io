---
layout: post
title: agf-test - Détermination du répertoire racine des ressources de test
tags: [framework-1-73,codjo-test]
---
Une méthode a été ajoutée à ```PathUtil``` qui permet de déterminer le répertoire racine des ressources de test (```findTestResourcesDirectory(...)```).

<u>Exemple</u>
```java
assertEquals(baseDir + "src/test/resources", PathUtil.findTestResourcesDirectory(MyTest.class));
```
