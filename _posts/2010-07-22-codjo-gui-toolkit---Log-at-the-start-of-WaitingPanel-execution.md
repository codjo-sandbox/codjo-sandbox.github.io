---
layout: post
title: agf-gui-toolkit - Log at the start of WaitingPanel execution
tags: [framework-1-157,codjo-gui-toolkit]
---
<u>Context</u>:
In order to check if a release-test contains the correct number of ```assertProgressDisplay``` tags, it is necessary to know how many times the ```WaitingPanel``` is called during the test.

<u>Description</u>:
A debug-level message is now logged at the beginning of the&nbsp;```exec(Runnable, Runnable)``` method of the ```WaitingPanel``` class. 