---
layout: post
title: agf-release-test - AssertVisible task timeout in milliseconds
tags: [framework-1-169,codjo-release-test]
---
<u>Context</u>:
Some ```capri``` release tests failed because of an ```assertVisible``` timeout.
```assertVisible``` task used this timeout as if it was in seconds whereas all assert timeout must be in milliseconds.

<u>Description</u>:
```AssertVisibleStep``` has been modified to work with a timeout in milliseconds.

see: [[framework:codjo-release-test - Tags IHM#assertVisible]]