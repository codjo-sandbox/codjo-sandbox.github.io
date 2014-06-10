---
layout: post
title: agf-agent - Catch all errors produced by a behaviour
tags: [framework-1-187,codjo-agent]
---
<u>Context</u>
Several bugs have been found in the latest releases of SAM, so we need to improve the overall stability of the agents (in order to give us more feedback on errors).

<u>Description</u>
We add a behaviour wrapping mechanism in order to catch all the unmanaged error thrown by an agent. Of course this mechanism should not be used for a long time (a kind of "desperate action"). Beware that this wrapping mechanism does not work for JADE protocols (Contract Net, Request...).

**Example**: The following code will protect the agent from any errors thrown by the ```badCodedBehaviour```. All the errors will be logged via ```Log4J```.
```java
@Override
protected void setup() {
    ...
    addBehaviour(Behaviour.thatNeverFails(new BehaviourWithBugs());
    ...
}
```

**Example**: It's also possible to provide a specific error handler.
```java
@Override
protected void setup() {
    ...
    addBehaviour(thatNeverFails(new BehaviourWithBugs(), new UncaughtErrorHandler() {
            public void handle(Throwable error, Behaviour behaviour) {
                // Do a specific error management
            }
        });
    ...
}
```
