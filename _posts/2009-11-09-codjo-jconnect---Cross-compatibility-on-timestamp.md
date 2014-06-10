---
layout: post
title: agf-jconnect - Cross compatibility on timestamp
tags: [framework-1-121,codjo-jconnect]
---
<u>Context</u>:
The library ```[[codjo-jconnect]]``` has been introduced to assume cross compatibility with jconnect 5.2.

During the deployment, a difference between jconnect 5.2 and the ```codjo-jconnect``` wrapper has been raised on the statements ```setTimestamp``` methods with ```null``` value. The inserted values were:
* ```1970-01-01 00:00:00``` with jconnect 5.2,
* ```null``` with the wrapper.

Even if the wrapper behaviour seems right, it is not compatible with jconnect 5.2. 

<u>Description</u>: 
The wrapper behavior has been **temporarily** changed to match the "jconnect 5.2" behaviour.
