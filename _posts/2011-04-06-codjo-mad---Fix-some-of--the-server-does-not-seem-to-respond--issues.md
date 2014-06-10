---
layout: post
title: agf-mad - Fix some of "the server does not seem to respond" issues
tags: [framework-1-193,codjo-mad]
---
<u>Context</u>
In order to fix some of "the server does not seem to respond" issues, the ```LoginEventSynchroniser``` class from ```codjo-security``` has been templatized and put into ```agf-util```.

see: [[codjo-security update|framework:/2011/04/05/agf-security - Refactoring to use an EventSynchroniser], [creation of EventSynchroniser in agf-util|framework:/2011/04/06/agf-util - Add of an EventSynchronizer class]]

<u>Description</u>
The race condition during the start of the ```MadClientPlugin``` has been removed by using a multi-thread synchronisation mechanism (i.e. ```EventSynchronizer```)

