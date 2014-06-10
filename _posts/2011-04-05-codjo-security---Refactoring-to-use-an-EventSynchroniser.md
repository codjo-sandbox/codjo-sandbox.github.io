---
layout: post
title: agf-security - Refactoring to use an EventSynchroniser
tags: [framework-1-193,codjo-security]
---
<u>Context</u>
In order to fix some of "the server does not seem to respond" issues, the ```LoginEventSynchroniser``` class from ```codjo-security``` has been templatized and put into ```agf-util```.

see: [[creation of EventSynchroniser in codjo-util|framework:/2011/04/06/agf-util - Add of an EventSynchronizer class], [issue fix in agf-mad|/2011/04/06/agf-mad - Fix some of "the server does not seem to respond" issues]]

<u>Description</u>
Remove of the ```LoginEventSynchroniser``` class (All usages has been replaced by an ```EventSynchroniser```). 

