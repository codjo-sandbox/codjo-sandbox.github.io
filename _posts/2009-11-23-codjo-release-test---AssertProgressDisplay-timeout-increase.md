---
layout: post
title: agf-release-test - AssertProgressDisplay timeout increase
tags: [framework-1-123,codjo-release-test]
---
<u>Context{</u>}
The "waiting panel" GUI displays when processing takes a long time.
The default timeout (15 seconds) may be insufficient in some cases.


<u>Description{</u>}
The default value has been set to 50 seconds.

see: [[codjo-release-test|agf-release-test - Tags IHM#assertProgressDisplay]]