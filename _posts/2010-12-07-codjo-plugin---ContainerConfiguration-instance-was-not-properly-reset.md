---
layout: post
title: agf-plugin - ContainerConfiguration instance was not properly reset
tags: [framework-1-177,codjo-plugin]
---
<u>Context</u>:
We overrode ```configureContainer()``` of ```ApplicationCore``` in ```scribe``` in order to set parameters to ```ContainerConfiguration```.
Next, when we retry to login after a failed attempt, we could not get the newly created ```ContainerConfiguration```.


<u>Description</u>:
A new ```ContainerConfiguration``` was created but the old instance was left over in the ```global components```.
It has been fixed.
