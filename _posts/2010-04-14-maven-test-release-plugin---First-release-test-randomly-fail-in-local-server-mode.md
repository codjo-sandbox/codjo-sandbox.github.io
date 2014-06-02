---
layout: post
title: maven-test-release-plugin - First release test randomly fail in local server mode
tags: [framework-1-142,maven-test-release-plugin,resolution-of-brin,hot-topics]
---
{info}Resolution of BRIN{info}

<u>Context</u>:
```aaam``` and ```smart``` integration builds sometimes failed in an unexpected manner.

<u>Description</u>:
```aaam``` and ```smart``` integration builds run in local server mode. In all failure cases, there is a problem during ```stop-server``` step which run in time-out for an unknown reason.
A retry mechanism has been implemented in ```stop-server``` step to bypass this problem.
