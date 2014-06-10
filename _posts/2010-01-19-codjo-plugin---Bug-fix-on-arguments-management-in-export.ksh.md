---
layout: post
title: agf-plugin - Bug fix on arguments management in export.ksh
tags: [framework-1-130,codjo-plugin,hot-topics]
---
<u>Context</u>
A bug has been introduced during the development of [[framework:/2009/12/14/codjo-plugin - Custom parameters in export.ksh]]. 

If only three arguments were given to the script, it failed due to a bad shell instruction use.

<u>Description</u>
The bug has been fixed.
