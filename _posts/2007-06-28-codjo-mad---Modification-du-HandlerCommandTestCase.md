---
layout: post
title: agf-mad - Modification du HandlerCommandTestCase
tags: [codjo-mad,framework-1-4]
---
Modification du ```HandlerCommandTestCase``` : 

* L'utilisation d'un fichier Tokio est maintenant optionnel. Il n'est plus nécessaire de surcharger la méthode ```initTokio()```.

* Ajout d'un getter sur le ```JdbcFixture``` du TestCase.

