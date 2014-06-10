---
layout: post
title: agf-standalone-common - Test DisplayInternalFrameActionTest added and minor modification
tags: [codjo-standalone-common,framework-1-132]
---
<u>Context</u>

   * There was no unit test for the method ```buildWindow()``` in the class ```WindowFactory```.
   * The line ```windowClass.getClass().getConstructor(getClassArguments())``` wrongly got the constructor of the super-class.

<u>Description</u>

   * Now the unit test has been added.
   * The line ```windowClass.getClass().getConstructor(getClassArguments())``` has been replaced by ```windowClass.getConstructor(getClassArguments())``` and gets the good constructor.
