---
layout: post
title: agf-pom - Change plugin's dependencies
tags: [framework-2-26,codjo-pom,hot-topics]
---
<u>Context</u>:
When ```codjo-datagen``` or ```codjo-release-test``` librairies are switch to SNAPSHOT, the corresponding plugin have to be switch to SNPASHOT too.

<u>Description</u>:
The version of the librairies have been put into its plugin's dependencies.
Now when a SNAPSHOT is put on one of these librairies it's plugin knows the SNAPSHOT (the version is also change in its dependencies by the ```swith-to-snapshot``` goal).
