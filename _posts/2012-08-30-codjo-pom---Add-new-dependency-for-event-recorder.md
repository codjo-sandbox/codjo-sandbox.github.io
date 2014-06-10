---
layout: post
title: agf-pom - Add new dependency for event-recorder
tags: [framework-2-30,codjo-pom,hot-topics]
---
<u>Context</u>:
To be able to upload event-recorder in github, we have to rename it from codjo-event-recorder to codjo-tools-event-recorder.

<u>Description</u>:
Since event-recorder's artifact has changed, we have to add a new dependency.
For compatibility reason, we kept the old one.

see: https://github.com/codjo/codjo-pom/pull/30

