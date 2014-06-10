---
layout: post
title: agf-release-test - Fix validate and cancel steps thread issue
tags: [framework-1-198,codjo-release-test,jdk16-migration]
---
<u>Context</u> 
During the JDK 6 migration impact study, we discovered that the steps ```validate``` and ```cancel``` used in the edit cell were not performed in the Swing Thread.

see: [[jdk16-migration]]

<u>Description</u> 
Now the two steps are executed in the Swing thread.
