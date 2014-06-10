---
layout: post
title: agf-mad - HandlerCommandTestCase - gestion du user et du mode non-transactionnel
tags: [codjo-mad,framework-1-38]
---
La classe HandlerCommandTestCase permettant de tester unitairement les HandlerCommand permet à présent :
* de gérer correctement les connexions en mode non-transactionnel.
* de spécifier un utilisateur à associer au contexte d'exécution du handler.

```
public class MyHandlerCommandTest extends HandlerCommandTestCase {

    @Override
    protected void setUp() throws Exception {
        super.setUp();
        setUser("DARK_VADOR");
    }

...
```