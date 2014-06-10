---
layout: post
title: agf-workflow - Sort arguments map
tags: [framework-1-198,codjo-workflow,jdk16-migration,codjo-broadcast,codjo-segmentation,codjo-imports]
---
<u>Context</u>
During the JDK 6 migration impact study, we discovered that the arguments of Workflow requests were not sorted. This behaviour can lead to testing issues.

see: [[framework:jdk16-migration]]

<u>Description</u>
The arguments are now sorted.
Some unit tests have been corrected to take into account the order.