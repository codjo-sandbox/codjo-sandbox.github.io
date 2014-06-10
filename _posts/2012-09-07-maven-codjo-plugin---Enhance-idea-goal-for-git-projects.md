---
layout: post
title: maven-agf-plugin - Enhance idea goal for git projects
tags: [framework-2-32,maven-codjo-plugin,hot-topics]
---
<u>Context</u>
When using ```codjo:idea``` with a git project the version control system is not well recognized by IntelliJ.


<u>Description</u>
The scm name was set to ```git``` instead of ```Git```, as the value was taken from the scm tag in the pom.xml.
