---
layout: post
title: agf-agent - Add log string mechanism to Story
tags: [framework-2-9,codjo-agent]
---
<u>Context</u>

For SAM we developed some utility methods that could be leveraged at a Framework level.

<u>Description</u>

A Story can now easily interact with a ```LogString```. Two new methods ```logInfo(...)``` and ```assertLog(...)``` have been added to the record mechanism.

Exemple: 
```
story.record()
      .logInfo(log, "hello world");

story.record()
      .assertLog(log, "hello world");

story.execute();
```

