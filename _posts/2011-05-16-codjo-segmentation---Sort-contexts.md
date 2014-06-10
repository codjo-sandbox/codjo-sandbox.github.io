---
layout: post
title: agf-segmentation - Sort contexts
tags: [framework-1-198,codjo-segmentation,jdk16-migration]
---
<u>Context</u>
During the JDK 6 migration impact study, we discovered that the different contexts (those wich extends ```AbstractContext<K, T>```) were not sorted. This behaviour leads to testing issues.

see: [[framework:jdk16-migration]]

<u>Description</u>
The contexts are now sorted, since we use a ```TreeMap``` instead of an ```HashMap```.

