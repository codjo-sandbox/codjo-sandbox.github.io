---
layout: post
title: agf-test - Comparaison avec arguments optionnels ou expressions regulières pour les tests d'appels journalisés
tags: [framework-1-114,codjo-test,hot-topics]
---
La classe ```LogString``` accepte deux nouveaux types d'arguments à sa méthode ```assertContent``` :
** ```String...``` : permet de tester que **chacun** des éléments apparaissant dans la liste des arguments est bien journalisé **dans l'ordre donné*
** ```Pattern``` : permet de tester que l'expression régulière donnée correspond bien à **l'intégralité* des appels journalisés.

Exemple avec les ellipses
```
logString.assertContent("setUp(connection/1234)",
                        "createStatement()",
                        "executeQuery(query@1234)",
                        "tearDown(connection/1234)");
```

Le même exemple avec une expression régulière
```
logString.assertContent(Pattern.compile("setUp.connection/(\\d+)., "
                                        + "createStatement.., "
                                        <u> "executeQuery.</u>, "
                                        + "tearDown.connection/\\1."));
```

{tip:title=Expression régulière}
Notez l'utilisation de ```.``` à la place des paranthèses englobant les arguments de méthodes et qu'il aurait fallu échapper comme ceci:
{noformat}createStatement\\(\\){noformat}

Notez également l'utilisation d'un groupe capturant sur la première ligne pour la méthode ```setUp```, réutilisé sur la dernière ligne pour la méthode ```tearDown``` : cela permet de vérifier que la connection passée en argument de ```setUp``` est bien celle qui est passée en argument de ```tearDown```.
{tip}