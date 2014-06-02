---
layout: post
title: maven-delivery-plugin - Inclusion de fichier KSH local
tags: [framework-1-10,maven-delivery-plugin]
---
Il est maintenant possible de spécifier des fichiers KSH local pour les livrables batch.

Dans le fichier ```pom.xml``` du projet (configuration du plugin delivery).

```xml
<includes>
    <include>
        <file>src/test/resources/assembly/local-batch-file.ksh</file>
        <output>import.ksh</output>
    </include>
    <include>
        <file>src/test/resources/assembly/local-batch-file.ksh</file>
    </include>
</includes>
```

Si la balise ```output``` n'est pas précisé le nom du fichier est pris en compte.

