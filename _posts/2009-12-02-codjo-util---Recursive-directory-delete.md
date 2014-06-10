---
layout: post
title: agf-util - Recursive directory delete
tags: [framework-1-124,codjo-util]
---
<u>Context</u>:
A recursive delete for directory was needed for the ```maven-test-release-plugin```.

<u>Description</u>:
It has been implemented.

<u>Example</u>:
```java
  FileUtil.deleteRecursively(new File("c:/Dev"));
```
