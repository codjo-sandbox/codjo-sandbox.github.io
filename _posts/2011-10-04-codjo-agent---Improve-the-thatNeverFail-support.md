---
layout: post
title: agf-agent - Improve the thatNeverFail support
tags: [codjo-agent,framework-2-1]
---
<u>Context</u>
For solving the BRIN [["Le batch de segmentation ne démarre pas"|http://wp-sic:8080/pyp/edit.html?id=0e1da8c1-8c16-4b47-b795-8e57944d2bb8]], we need to have a fail safe behaviour for the ```AmsListenerBehaviour```.

<u>Description</u>

Starting today, the ```AmsListenerBehaviour``` supports the ```Behaviour.thatNeverFails(..)``` mechanism.

<u>Example</u>:
```java
public class MyAgent extends Agent {
  ...
  @Override
  protected void setup() {
    AmsListenerBehaviour amsListener = ...;
    ams.setAgentDeathHandler(...);

    addBehaviour(thatNeverFails(amsListener));
    ...
    }
}
```

