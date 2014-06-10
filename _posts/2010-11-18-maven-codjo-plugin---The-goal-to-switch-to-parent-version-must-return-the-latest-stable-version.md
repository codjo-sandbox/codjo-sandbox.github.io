---
layout: post
title: maven-agf-plugin - The goal to switch to parent version must return the latest stable version
tags: [framework-1-175,maven-codjo-plugin,resolution-of-brin,hot-topics]
---
<u>Context</u>:
The ```agf:switch-to-parent-release``` goal may return a release candidate version of the framework.
It is preferable for that goal to always return a stable version of the framework.

<u>Description</u>:
The goal has been modified in order to return only the latest stable version.
