---
layout: post
title: agf-release-test - New web task assertImage to assert web "img"
tags: [framework-1-165,codjo-release-test]
---
<u>Context</u>:
For magic, we needed to check <img> tags.

<u>Description</u>:
It is now possible to check <img> by using the new ```assertImage``` web task.

```xml
<assertImage src="MINT_PRODUCTION/logo.png"/>
``` 

see: [[framework:codjo-release-test - Tags web#assertImage]]