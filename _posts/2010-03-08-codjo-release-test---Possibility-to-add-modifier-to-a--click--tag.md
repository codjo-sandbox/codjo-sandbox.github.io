---
layout: post
title: agf-release-test - Possibility to add modifier to a "click" tag
tags: [framework-1-137,codjo-release-test,hot-topics]
---
<u>Context :</u>
In the aim of testing a column's deselection, it was needed to add a modifier to simulate the ```ctrl click``` in test-releases.

<u>Description :</u>
By now, specifying the ```modifier``` parameter's value, the ```click``` tag is able to simulate the "control" and "shift" modifiers.

```xml
   <click name="myTable" row="1" modifier="ctrl" />
```

```xml
   <click name="myButton" modifier="shift" />
```

see: [[framework:codjo-release-test - Tags IHM#Click]]