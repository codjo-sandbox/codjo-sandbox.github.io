---
layout: post
title: agf-agent - Fix bug in the Aid
tags: [framework-1-185,codjo-agent]
---
<u>Context</u>
Using Agent in SAM we faced some strange and inconsistant behaviour due to some bugs in the Aid. The local Aid Name and Global Aid were misunderstood and were badly mixed.

<u>Description</u>
A deep internal modification has been made to try to fix the blurry between the 2 notions.

For information: 
* an AID follow this pattern : ```<agent-nick-name>@<Home Agent Platform>```. e.g. ```john@A7WX063:35714/JADE```
* a local AID is an AID in which we do not specify the Home Agent Platform (JADE will assume the current started one)
* a global AID is an AID in which we specify the Home Agent Platform.
```
fixture.startContainer(ConnectionType.NO_CONNECTION);
Aid globalAid = new Aid("john@localhost:-1/JADE", false);
Aid localAid = new Aid("john");

assertTrue(globalAid.equals(localAid));
```