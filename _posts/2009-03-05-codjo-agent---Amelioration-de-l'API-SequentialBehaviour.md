---
layout: post
title: agf-agent - Amélioration de l'API SequentialBehaviour
tags: [framework-1-86,codjo-agent]
---
L'API ```SequentialBehaviour``` a été modifiée afin de suivre le modèle [[fluent interface|http://www.martinfowler.com/bliki/FluentInterface.html]].

<u>Exemple</u>
```
class KamikazeAgent extends Agent {
  ...
  @Override
  protected void setup() {
      addBehaviour(SequentialBehaviour
            .wichStartsWith(triggerSessionStopEvent())
            .andThen(killThis(ambassador))
            .andThen(commitSuicide()));
  }
  ...
}
```
