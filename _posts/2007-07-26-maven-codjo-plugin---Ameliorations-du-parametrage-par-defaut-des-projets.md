---
layout: post
title: maven-agf-plugin - Améliorations du paramétrage par défaut des projets
tags: [maven-codjo-plugin,framework-1-7]
---
Il est dorénavant possible de fournir une configuration par défaut pour les tests JUnit dans le fichier idea.xml :
```
<idea>
    ...
    <defaultJUnitConfiguration>
        <vmParameter> ... </vmParameter>   -- VM parameters
        <parameter> ... </parameter>       -- Test runner parameters
        <workdir> ... </workdir>           -- Working directory
    </defaultJUnitConfiguration>
    ...
</idea>
```

Autres améliorations mineures du paramétrage :
* Option "do not upgrade" par défaut pour subversion
* Librairies externes et modules cachés dans la vue package
* Lancement des run configuration sans afficher la page de settings