---
layout: post
title: agf-agent - Improve support of the fail safe mechanism
tags: [framework-1-188,codjo-agent]
---
<u>Context</u>
In the previous framework version the ```Behaviour.thatNeverFails(..)``` has been implemented (see [[framework:/2011/02/14/codjo-agent - Catch all errors produced by a behaviour]]), but this method didn't support the standard JADE protocol (Contract net, etc.).


<u>Description</u>
We add the support for JADE protocols (Contract Net, Subscribe, etc.).
