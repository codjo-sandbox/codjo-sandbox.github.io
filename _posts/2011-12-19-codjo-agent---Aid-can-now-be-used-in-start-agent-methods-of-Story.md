---
layout: post
title: agf-agent - Aid can now be used in start agent methods of Story
tags: [framework-2-10,codjo-agent]
---
<u>Context</u>

For SAM, we need more utility methods in ```Story```.

<u>Description</u>

We can now use an ```Aid``` object as a name for ```Agent``` in the various start methods.

```java
story.record().startTester(new Aid("Murtaugh"))
...
story.record().startAgent(new Aid("Riggs"), new LethalWeaponAgent())
...
```

