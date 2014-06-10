---
layout: post
title: agf-mad - Error management improvement when building an handler
tags: [framework-1-123,codjo-mad]
---
<u>Context</u>:

It's sometimes difficult to identify why an ```Handler``` can't be built. The causes can be multiple (unknwon ```Handler```, unbuildable ```Handler```) but ```mad``` didn't make the difference.

<u>Description</u>:

The error management has been improved, the root exception is now thrown when an ```Handler``` can't be built.

