---
layout: post
title: agf-security - Bug in LoginWindow when using the default splash image
tags: [framework-1-177,codjo-security,hot-topics]
---
<u>Context</u>:
After a recent ```roses``` delivery, users were unable to log: the splash image was not found, an exception blocked the ```gui```.

<u>Description</u>:
```Roses``` don't define a splash image and therefore must use the default one.
But while moving ```LoginWindow``` to ```codjo-security```, we have introduced the bug described above.
It has been fixed.

see: [[framework:/2010/11/25/safe - The login window has been moved from mad to security]]
