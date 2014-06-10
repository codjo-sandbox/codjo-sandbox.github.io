---
layout: post
title: agf-mad - Amélioration de MadServerFixture
tags: [framework-1-19,codjo-mad]
---
Il est maintenant possible de mettre plusieurs requêtes en file d'attente dans la MadServerFixture. Ainsi les méthodes qui envoient plusieurs requêtes deviennent testables.

Exemple :
```
MadServerFixture fixture = ... ;
Result result1 = MadServerFixture.createResult(
    new String[[]]{ ... },
    new String[[][]]{ ... } });
Result result2 = MadServerFixture.createResult(
    new String[[]]{ ... },
    new String[[][]]{ ... } });
fixture.queueServerResult(result1, result2);
uneMethodeQuiFaitDeuxAppelsMad();
```

De nouvelles méthodes permettent également de récupérer et d'asserter le contenu des requêtes précédemment envoyées :
```
MadServerFixture fixture = ... ;
fixture.getSentRequests( 5 );
fixture.getXmlSentRequest( 5 );
fixture.assertSentRequests( "<xml> ....", 5 );
```