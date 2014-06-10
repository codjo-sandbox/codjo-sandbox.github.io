---
layout: post
title: agf-release-test - Possibilité de tester les codes d'erreurs http
tags: [framework-1-116,codjo-release-test,hot-topics]
---
Il est maintenant possible de vérifier les codes d'erreurs http (404, ...).
* l'attribut ```failOnError``` a été ajouté à la balise ```web-test``` (par défaut à ```true```). Il indique si le test doit échouer dans le cas où le serveur renvoie un état différent de ```OK```.
* la balise ```assertPage``` a été enrichie d'un attribut ```errorCode``` permettant de vérifier l'état de la page.

<u>Exemple</u> :
```xml
<web-test url="http://localhost:8080" failOnError="false">
  <assertPage errorCode="404"/>
</web-test>
```

cf. [[codjo-release-test - Tags web]]
