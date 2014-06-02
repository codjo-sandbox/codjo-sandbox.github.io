---
layout: post
title: maven-agf-plugin - Update of release goal
tags: [framework-2-14,maven-codjo-plugin]
---
<u>Context</u>
Since the file hierarchy of the pom project changed the release goal of the codjo plugin was not working anymore.

<u>Description</u>
Now the plugin is treating pom files in all subdirectories.