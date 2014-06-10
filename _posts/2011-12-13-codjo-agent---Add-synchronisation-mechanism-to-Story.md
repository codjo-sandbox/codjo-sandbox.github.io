---
layout: post
title: agf-agent - Add synchronisation mechanism to Story
tags: [framework-2-9,codjo-agent]
---
<u>Context</u>

For SAM we developed some utility methods that could be leveraged at a Framework level.

<u>Description</u>

A Story can now be easily synchronised using a ```Semaphore```. Two new methods ```acquire(...)``` and ```release(...)``` have been added to the record mechanism.

<u>Example</u>: _Action 1_ will be executed before _Action 2_
```java
Semaphore semaphore = new Semaphore();

story.record().startTester("first")
      .perform(/**Action 1**/)
      .then()
      .release(semaphore);

story.record()
      .acquire(semaphore);

story.record()
      .addAction(/**Action 2**/);

story.execute();
```

