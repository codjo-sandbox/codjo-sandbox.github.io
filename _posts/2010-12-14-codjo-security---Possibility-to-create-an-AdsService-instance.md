---
layout: post
title: agf-security - Possibility to create an AdsService instance
tags: [framework-1-178,codjo-security]
---
<u>Context</u>:
Working on ```magic```, we needed to create an ```AdsService``` instance.

<u>Description</u>:
A static method has been added in ```AdsSecurityManager``` class:
```java
AdsService buildAdsService(Map<String, String> parametersMap)
```
