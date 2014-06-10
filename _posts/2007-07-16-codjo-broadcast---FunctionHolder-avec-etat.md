---
layout: post
title: agf-broadcast - FunctionHolder avec état
tags: [framework-1-5,codjo-broadcast]
---
Ajout d'une méthode permettant d'instancier un ```FunctionHolder``` en fonction d'un contexte d'export particulier. 

Sur la classe ```FunctionHolder``` :
```java
createFunctionHolder(Context context) {
   return getFunctionHolder();
}
```

Cette méthode est pratique car elle permet de garder un état durant un export. Par exemple la date d'export J-1.
