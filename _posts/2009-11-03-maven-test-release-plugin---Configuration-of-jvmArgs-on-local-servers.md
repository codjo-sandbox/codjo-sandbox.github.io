---
layout: post
title: maven-test-release-plugin - Configuration of jvmArgs on local servers
tags: [framework-1-120,maven-test-release-plugin,hot-topics]
---
During release tests, when the server was running locally, it was not possible to customize the memory allocation for the server's jvm.

A new attribute ```localServerJvmArgs``` has been added to the configuration of the plugin, allowing to pass jvmArgs parameters.

<u>Example</u>:
```xml
<plugin>
  <groupId>com.agf.maven.mojo</groupId>
  <artifactId>maven-test-release-plugin</artifactId>
  <configuration>
    <serverMainClass>${serverMainClass}</serverMainClass>
    <localServerJvmArgs>-Xmx128m</localServerJvmArgs>
    <server>
      <groupId>com.agf.sam</groupId>
      <artifactId>sam-server</artifactId>
      <classifier>assembly</classifier>
    </server>
  </configuration>
</plugin>
```

see: [[maven-test-release-plugin]]