---
layout: post
title: agf-agent - Improve assert log string mechanism
tags: [framework-2-11,codjo-agent]
---
<u>Context</u>

For SAM we developed some utility methods that could be leveraged at a Framework level.

<u>Description</u>

One new method ```assertLogContains(...)``` has been added.

<u>Example</u> 
```
story.record()
      .logInfo(log, "hello world");

story.record()
      .assertLogContains(log, "world", "hello");

story.execute();
```

