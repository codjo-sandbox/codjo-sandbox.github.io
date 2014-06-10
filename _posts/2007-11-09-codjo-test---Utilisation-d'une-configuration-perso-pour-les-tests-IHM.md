---
layout: post
title: agf-test - Utilisation d'une configuration perso pour les tests IHM
tags: [framework-1-19,codjo-test]
---
Il est désormais possible d'utiliser une configuration personnelle dans les tests IHM.

<u>Exemple</u> : Pour créer une configuration "test", ajouter les lignes suivantes dans le fichier test-release.config :
```
gui.test.class = com.agf.bidon.Bidon
gui.test.method = main
gui.test.arg.0 = ${defaultTestUser}
gui.test.arg.1 = ${defaultTestUserPassword}
gui.test.arg.2 = ${serverHost}
gui.test.arg.3 = ${serverPort}
```
&nbsp;Pour appeler cette configuration dans un test IHM, passer le paramètre test à l'attribut gui dans la balise gui-test :
```
    <gui-test gui="test">
```
&nbsp;Dans cet exemple, le test appellera la classe Bidon au démarrage.
\\