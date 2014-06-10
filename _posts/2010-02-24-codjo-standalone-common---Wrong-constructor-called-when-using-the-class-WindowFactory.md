---
layout: post
title: agf-standalone-common - Wrong constructor called when using the class WindowFactory
tags: [framework-1-134,codjo-standalone-common]
---
<u>Context</u>:

The method ```buildWindow()``` of the class ```WindowFactory``` generated the wrong constructor.It was not based on the constructor arguments but returned the first one.

Recently, a modification was made so that the good constructor is generated, according to the number and type of arguments.(See: [[framework:/2010/01/19/codjo-standalone-common - Wrong constructor called when using the class WindowFactory]]).

However, even after this modification, the method ```buildWindow()``` didn't always return the good constructor.

<u>Description</u>:

A parameter ```classes``` containing the types of the arguments has been added to the constructor of ```DisplayInternalFrameAction```. These arguments are then used in the method ```buildWindow()``` of the class ```WindowFactory``` to return the good constructor.