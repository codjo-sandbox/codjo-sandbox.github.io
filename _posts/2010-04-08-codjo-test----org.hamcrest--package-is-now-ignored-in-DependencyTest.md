---
layout: post
title: agf-test - "org.hamcrest" package is now ignored in DependencyTest
tags: [framework-1-142,codjo-test]
---
<u>Context</u>:
Some ```DependencyTest``` "manually" ignores ```org.hamcrest``` package, whereas it is a specific test package.

<u>Description</u>:
```org.hamcrest``` package is now ignored by default in ```PackageDependencyTestCase```.