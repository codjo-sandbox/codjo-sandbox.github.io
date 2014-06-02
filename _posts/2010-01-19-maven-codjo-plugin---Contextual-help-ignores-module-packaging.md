---
layout: post
title: maven-agf-plugin - Contextual help ignores module packaging
tags: [framework-1-130,maven-codjo-plugin,hot-topics]
---
<u>Context</u>:
The ```agf:help``` goal didn't work inside some modules (sql, datagen, ...) of many applications.

<u>Description</u>:
```agf:help``` is a contextual help which depends upon module.
Before, the goal took account of the module name and packaging.
Now, only the module name is used.

<u>Example</u>:
```
C:\dev\project\mint\mint-sql>mvn agf:help
```

see: [[framework:maven-codjo-plugin]]