---
layout: post
title: agf-agent - Possibility to assert log using regular expression
tags: [framework-1-129,codjo-agent]
---
<u>Context</u>:
An ```codjo-administration``` agent test randomly failed when asserting a log.
This was due to unordered calls on ```logString```.

<u>Description</u>:
New methods ```Assertion  log(LogString, Pattern)``` and ```Assertion logAndClear(LogString, Pattern)``` have been created.
They allow to use regular expression and thus allow more flexibility when asserting logs.

<u>Example</u>:
```java
story.record().addAssert(AgentAssert.log(logString, new Pattern("(.**handleActionStarted\\(\\).**){3}")
```
