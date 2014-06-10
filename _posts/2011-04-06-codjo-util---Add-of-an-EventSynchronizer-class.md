---
layout: post
title: agf-util - Add of an EventSynchronizer class
tags: [framework-1-193,codjo-util]
---
<u>Context</u>
In order to fix some of "the server does not seem to respond" issues, the ```LoginEventSynchroniser``` class from ```codjo-security``` has been templatized and put into ```agf-util```.

see: [[codjo-security update|framework:/2011/04/05/agf-security - Refactoring to use an EventSynchroniser], [issue fix in agf-mad|/2011/04/06/agf-mad - Fix some of "the server does not seem to respond" issues]]

<u>Description</u>
Add of the ```EventSynchroniser``` class.

<u>Example</u> of usage
```java
  // initialization
  EventSynchronizer<String> synchronizer = new EventSynchronizer<String>()

  ...
  // in Thread A - consumer
  String event = synchronizer.waitEvent();
  System.out.println("received event = " + event);

  ...
  // in Thread B - producer
  ... produce an event
  synchronizer.receivedEvent(event)
```
