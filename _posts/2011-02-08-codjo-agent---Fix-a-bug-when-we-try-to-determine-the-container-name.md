---
layout: post
title: agf-agent - Fix a bug when we try to determine the container name
tags: [framework-1-186,codjo-agent]
---
<u>Context</u>
A bug has been found in the last release of SAM when the code tries to determine the container name of an agent AID.

<u>Description</u>
The utility method ```getContainerName()``` of the ```Aid``` class has been fixed.
