---
layout: post
title: agf-release-test - WaitingPanel assertion improvements
tags: [framework-1-171,codjo-release-test]
---
<u>Context</u>:
```<assertVisible name="waitingPanel" expected="false"/>``` occasionally failed when two or more internal frames were displayed.

<u>Description</u>:
* When an internal frame becomes deselected, its ```GlassPane``` becomes visible making ```assertVisible``` fail.
```AssertVisibleStep``` has been modified to make assertion only on the currently selected internal frame.
* ```AssertProgressDisplay``` could detect ```WaitingPanel``` in invisible internal frames.
It has been modified to ignore invisible internal frames.

see: [[framework:codjo-release-test - Tags IHM#assertVisible] and [framework:agf-release-test - Tags IHM#assertProgressDisplay]]