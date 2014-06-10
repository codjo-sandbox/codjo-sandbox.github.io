---
layout: post
title: agf-pom - POM Refactoring in order to handle external library compilation
tags: [framework-2-13,codjo-pom,hot-topics]
---
<u>Context</u>

Most of our libraries do not compile outside our specific environment, we need to set-up a more lightweight POM that can be used everywhere.

<u>Description</u>
We introduced a new intermediate pom, called **codjo-pom-agif**, for legacy management. It contains all the specific configuration used in our environment.

We introduced a new pom, called **codjo-pom-external** as a  new root pom for all codjo components (libraries, plugins, etc) -  Can be used by maven 2 & 3

* AGIF Context
```
mvn clean install 
```
* External context
```
mvn clean install -Dexternal=true 
```
