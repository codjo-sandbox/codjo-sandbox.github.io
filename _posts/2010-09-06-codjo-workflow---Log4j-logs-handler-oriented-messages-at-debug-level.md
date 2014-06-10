---
layout: post
title: agf-workflow - Log4j logs handler-oriented messages at debug level
tags: [framework-1-163,codjo-workflow,parallel-workflow,hot-topics]
---
<u>Context</u>
Handlers are now managed by the framework workflow mechanism. As a result, the amount of ```log4j``` logs has increased dramatically. For example, MINT logs can only show an activity of 10 minutes on server-side.

<u>Description</u>
Handler-oriented messages are now logged at DEBUG level.
Other kinds of workflow messages are still logged at INFO level.
The ```codjo-mad``` library still logs the name of the handler being executed and the execution time at INFO level.

<u>Example</u>
```
14:39:16,536 INFO  com.agf.mad.common.Log - Execution du handler selectAllBenchs
14:39:16,536 INFO  com.agf.mad.common.Log - Traitement de la requete en 15 ms
```