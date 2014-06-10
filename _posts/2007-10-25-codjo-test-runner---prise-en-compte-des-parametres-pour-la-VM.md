---
layout: post
title: agf-test-runner - prise en compte des paramétres pour la VM
tags: [codjo-test-runner]
---
#### Procédure

Afin de pouvoir lancer les test release depuis IntelliJ tout en passant des paramètres à la machine virtuel de Java, suivre les instructions suivantes :

1. S'assurer avoir la dernière version de Bud installé

2. Dans le fichier ```test-release.config``` ajouter le paramètre suivant :
```
vmParameter = -Djava.library.path="${basedir}/../myapp-mymodule/target/dll"
```