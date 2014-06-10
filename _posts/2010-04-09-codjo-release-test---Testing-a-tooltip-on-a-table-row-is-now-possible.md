---
layout: post
title: agf-release-test - Testing a tooltip on a table row is now possible
tags: [framework-1-142,codjo-release-test,hot-topics]
---
<u>Context:</u>
AAAm projects needs to add tooltip on table rows. 

<u>Description:</u>
In order to test this behaviour, the step ```assertTooltip``` was modified. 
Now, it contains a ```row``` attribute which indicates the line to get tooltip on.

<u>Example:</u>
```
<assertTooltip name="pendingCashMovementsList" row="0" expected="Date de création: 2008-12-26 00:00:00.0"/>
```

see: [[framework:codjo-release-test - Tags IHM#assertTooltip]]
