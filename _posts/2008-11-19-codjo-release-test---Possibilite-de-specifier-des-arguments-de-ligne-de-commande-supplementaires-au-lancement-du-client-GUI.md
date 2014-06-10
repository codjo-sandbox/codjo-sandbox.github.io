---
layout: post
title: agf-release-test - Possibilité de spécifier des arguments de ligne de commande supplémentaires au lancement du client GUI
tags: [framework-1-70,codjo-release-test]
---
La balise ```<gui-test>``` accepte un nouvel attribut ```additionalArguments``` qui permet de spécifier des arguments de ligne de commande supplémentaires. Ceci permet de tester les configurations de lancement d'une application.

Exemple :
```
<gui-test additionalArguments="-arg valeur">
    ...
</gui-test>
```
La ligne de commande générée est de la forme :

```java ... <classe main> <arguments de test-release.config> <arguments supplémentaires>```