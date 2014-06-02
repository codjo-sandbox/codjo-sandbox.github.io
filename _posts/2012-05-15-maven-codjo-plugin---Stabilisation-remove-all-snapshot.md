---
layout: post
title: maven-agf-plugin - Stabilisation remove all snapshot
tags: [framework-2-20,maven-codjo-plugin]
---
<u>Context</u>
During the stabilisation phase, the "SNAPSHOT" are removed by the ```switch-to-release``` goal.
But some "SNAPSHOT" were still present in the dependencies of plugins.

<u>Description</u>
Now those "SNAPSHOT" are also removed (for real).