---
layout: post
title: agf-jconnect - Error 2402 thrown during executeUpdate
tags: [framework-1-122,codjo-jconnect]
---
<u>Context</u>:
During an executeUpdate() with ```codjo-jconnect```, an exception with error code 2402 was thrown.
The same code in jconnect 5.2 ran successfully.

<u>Description</u>:
To fix **temporarily** the problem, the exception has been catched in the wrapper. 