---
layout: post
title: agf-agent - Modification de l'interface Assertion
tags: [codjo-agent,framework-1-26]
---
Modification de l'interface décrivant une Assertion. La méthode ```check``` peut maintenant renvoyer n'importe qu'elle exception.

```java
AgentContainerFixture fixture = ....

fixture.setAssertTimeout(1000); // Optionnel
fixture.setMaxTryBeforeFailure(30); // Optionnel

fixture.assertUntilOk(new AgentAssert.Assertion() {
          public void check() throws SQLException, IOException {
            doSomeSqlAssert();
            doSomeFileAssert();
          }
        });
```
