---
layout: post
title: maven-database-plugin - Init from production can include all modules
tags: [framework-1-133,maven-database-plugin]
---
<u>Context</u>:
Benchmark comparison from production failed because it had non standard dependencies among modules.

<u>Description</u>:
Possibility to make an init from production including all modules has been added to the plugin.

<u>Example</u>:
```xml
<plugin>
  <groupId>com.agf.maven.mojo</groupId>
  <artifactId>maven-database-plugin</artifactId>
  <configuration>
    <fullInitFromProd>true</fullInitFromProd>
  </configuration>
</plugin>
```

see: [[framework:maven-database-plugin - init-from-prod]]