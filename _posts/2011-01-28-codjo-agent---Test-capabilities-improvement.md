---
layout: post
title: agf-agent - Test capabilities improvement
tags: [framework-1-185,codjo-agent]
---
<u>Context</u>
For SAM we need to add some new test features to codjo-agent.

<u>Description</u>

* In order to speed up some unit tests, we need to be able to use easily an ```AgentContainerFixture``` without external connection (standard mode for ```Story```). A new method ```startContainer(ConnectionType)``` has been added to ```AgentContainerFixture```.
<u>Example</u>
```
AgentContainerFixture fixture = new AgentContainerFixture();
...
fixture.startContainer(ConnectionType.NO_CONNECTION);
Aid johnAid = new Aid("john", LOCAL_NAME_AID);
assertEquals("john@localhost:-1/JADE", johnAid.getName());
```

* We add an utility class ```AgentStep``` to put together some factory method in order to build some common ```Step``` implementation.
<u>Example</u>
the method ```logInfo``` will do a log on the ```LogString```
```
story.record().startTester("second")
      .acquire(semaphore)
      .then()
      .perform(AgentStep.logInfo(log, "second"));
```

* The method ```addStep``` of ```Story``` has been renamed to ```perform``` and improved.
```
    story.record().startTester("first")
          .perform(logInfo(log, "first"))
          .then()
          .release(semaphore);
```

* We add the possibility to specify the sender of a message in the ```MessageBuilder```
```
story.record().startTester("so-called ams")
              .send(MessageBuilder.message(INFORM).from(AMS).to("other agent"));
```

* We add 2 utility methods in ```Story``` to handle easily ```Semaphore``` (```acquire``` & ```release```)
```
public void test_semaphore() throws Exception {
    Semaphore semaphore = new Semaphore();

    story.record().startTester("second")
          .acquire(semaphore)
          .then()
          .perform(logInfo(log, "second"));

    story.record().startTester("first")
          .perform(logInfo(log, "first"))
          .then()
          .release(semaphore);

    story.record().addAssert(log(log, "first, second"));

    story.execute();
}
```
