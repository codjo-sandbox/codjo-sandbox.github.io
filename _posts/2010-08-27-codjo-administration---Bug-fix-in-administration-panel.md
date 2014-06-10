---
layout: post
title: agf-administration - Bug fix in administration panel
tags: [codjo-administration,framework-1-162]
---
<u>Context</u>:
When changing the log directory in administration panel, new log files could be retrieved before the directory is changed.
This was failing a test randomly.


<u>Description</u>:
The two behaviours responsible for these actions are now added to a sequential behaviour and executed serially.

see [[framework:Guide Utilisateur IHM de codjo-administration]]