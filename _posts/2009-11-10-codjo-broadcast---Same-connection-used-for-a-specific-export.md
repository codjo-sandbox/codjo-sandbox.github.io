---
layout: post
title: agf-broadcast - Same connection used for a specific export
tags: [framework-1-121,codjo-broadcast]
---
<u>Context</u>:
GABI needed the same connection instance for each ```Selector``` for the broadcast process.

<u>Description</u>:
The connection is now the same instance for each call to ```Selector``` and ```PostBroadcaster```.

See [[Utilisation de codjo-broadcast]].