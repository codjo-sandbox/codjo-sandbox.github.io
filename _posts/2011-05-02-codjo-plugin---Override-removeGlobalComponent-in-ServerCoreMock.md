---
layout: post
title: agf-plugin - Override removeGlobalComponent in ServerCoreMock
tags: [framework-1-196,codjo-plugin]
---
<u>Context</u>
In order to remove duplicated code between Benchmark and Framework, we need to modify some framework libraries.

<u>Description</u>
In order to increase testability, the method ```removeGlobalComponent``` has been overrided in the ```ServerCoreMock```. 

<u>Example</u>
```
  ServerCoreMock core = new ServerCoreMock(new LogString("core", log));
  ...
  core.removeGlobalComponent(MyComponent.class)
  ...
  log.assertContent("core.removeGlobalComponent(MyComponent)");
```
