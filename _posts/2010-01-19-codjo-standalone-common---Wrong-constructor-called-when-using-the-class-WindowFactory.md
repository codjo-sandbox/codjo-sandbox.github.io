---
layout: post
title: agf-standalone-common - Wrong constructor called when using the class WindowFactory
tags: [codjo-standalone-common,framework-1-131]
---
<u>Context</u>

The ```buildWindow()``` method of the class ```WindowFactory``` generated the wrong constructor.
It was not based on the constructor arguments, but returned the first one.

<u>Description</u>

Now the good constructor is generated, according to the number and type of arguments.
