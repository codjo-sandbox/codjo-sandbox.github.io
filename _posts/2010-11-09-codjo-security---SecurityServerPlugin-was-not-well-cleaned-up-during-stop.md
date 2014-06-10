---
layout: post
title: agf-security - SecurityServerPlugin was not well cleaned up during stop
tags: [framework-1-173,codjo-security]
---
<u>Context</u>:
An error occurred while retrying to login to ```benchmark```.

<u>Description</u>:
While stopping ```SecurityServerPlugin```, an instance of ```StorageFactory``` remained in ```applicationCore```.
This has been fixed.