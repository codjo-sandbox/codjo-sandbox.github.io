---
layout: post
title: agf-release-test - Improvement of image assertion step
tags: [framework-2-15,codjo-release-test]
---
<u>Context</u>
In MINT, a release test failed in jdk6 version on ```assertComponentImage``` step.

<u>Description</u>
In order to fix this problem, the screenshot and comparison methods have been modified.
Size of pixel representation depends on workstation's hardware, so it was possible to obtain screenshots with different pixel sizes (24 or 32 bits).
So, instead of comparing the two ```BufferedImage``` byte by byte we are using a pixel comparison (pixels number and pixel RGB codes).