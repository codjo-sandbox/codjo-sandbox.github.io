---
layout: post
title: agf-broadcast - Custom parameters in BroadcastBatchPlugin
tags: [hot-topics,framework-1-126,codjo-broadcast]
---
<u>Context</u>: 
Mint application needs specific arguments for some export.

<u>Description</u>: 
```BroadcastBatchPlugin``` is now able to manage extra arguments, by putting them in the ```BroadcastRequest```.

<u>Example</u>:
In the ```Selector```, specific arguments are accessed as follows:

```
JobRequest jobRequest = (JobRequest)context.getParameter("jobRequest");
String argValue = jobRequest.getArguments().get("myCustomParam");
```

To test the customized export with the ```codjo-release-test``` API, arg line should be defined for both **local** and **remote** contexts with the ```set-property``` task:

```xml
<set-property name="command.line"
              localValue="-type broadcast -initiator TOTO -arg ${broadcast.output.dir}/MY_EXPORT.txt -date 2009-12-31 -myCustomParam aValue"
              remoteValue="TOTO MY_EXPORT.txt 2009-12-31 -myCustomParam aValue"/>

    <vtom user="TOTO" batchType="broadcast" returnCode="0">
        <arg line="${command.line}"/>
    </vtom>
```
This way to do is due to the current behaviour of the vtom task that runs a specific code for each execution context.