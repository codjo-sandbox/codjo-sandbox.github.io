---
layout: post
title: agf-pom - Exclusion de plexus-utils
tags: [codjo-pom,framework-1-33]
---
```plexus-utils``` a été mis en ```exclusion``` dans le ```super-pom``` :

```xml
...
<dependency>
  <groupId>org.apache.maven.reporting</groupId>
  <artifactId>maven-reporting-impl</artifactId>
  <version>2.0.4</version>
  <exclusions>
    <exclusion>
      <groupId>xml-apis</groupId>
      <artifactId>xml-apis</artifactId>
    </exclusion>
    <exclusion>
      <groupId>plexus</groupId>
      <artifactId>plexus-utils</artifactId>
    </exclusion>
  </exclusions>
</dependency>
...
```