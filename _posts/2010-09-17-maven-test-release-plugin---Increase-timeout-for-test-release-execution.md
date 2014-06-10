---
layout: post
title: maven-test-release-plugin - Increase timeout for test-release execution
tags: [framework-1-165,maven-test-release-plugin]
---
<u>Context</u>
The default timeout (2 hours) configured for test-release execution is too short for MINT needs (new tests have been added). It brought MINT to a huge amount of build failures upon SIC since a few weeks.

<u>Description</u>
It has been increased to 4 hours. Moreover, an explicit message is shown when the timeout expires.