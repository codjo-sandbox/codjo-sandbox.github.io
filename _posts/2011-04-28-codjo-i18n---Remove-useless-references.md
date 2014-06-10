---
layout: post
title: agf-i18n - Remove useless references
tags: [codjo-i18n,framework-1-196]
---
<u>Context</u>
Internationalizable objects were not removed in ```removeUselessReferences``` method.

<u>Description</u>
The ```removeUselessReferences``` method is modify to remove objects which are not used anymore.