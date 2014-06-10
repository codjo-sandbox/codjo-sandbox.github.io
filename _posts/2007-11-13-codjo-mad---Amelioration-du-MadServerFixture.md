---
layout: post
title: agf-mad - Amélioration du MadServerFixture
tags: [codjo-mad,framework-1-19]
---
Ajout de la possibilite de definir une strategie pour la réponse du serveur.

<u>Exemple</u> d'utilisation dans un des tests de ```MadConnectionPlugin```.

```java
madServerFixture.setServerMock(new MadServerFixture.ServerMock() {
    public Result[[] createResults(String[]] requestIds, String xmlRequest, long timeout) {
        log.call("createResults", timeout);
        return myResults;  
    }
});

plugin.getOperations().sendRequest(new CommandRequest(), 10);

log.assertContent("createResults(10)");

```
