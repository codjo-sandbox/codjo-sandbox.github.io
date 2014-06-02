---
layout: post
title: maven-agf-plugin - Add find-release-version goal
tags: [framework-2-26,maven-codjo-plugin]
---
<u>Context</u>
Pom metadata files are not up to date after a stabilisation.

<u>Description</u>
We added a goal ```find-release-version``` to be able to verify the framework version according to maven (since Nexus index can be desynchronised with the repo.codjo.net metadata).

This goal is also used to force Nexus to download new metadata.

see. http://wp-confluence/confluence/display/framework/maven-codjo-plugin
