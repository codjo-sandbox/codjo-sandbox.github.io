---
layout: post
title: agf-plugin - Fix temporary directory on UNIX server
tags: [framework-1-173,codjo-plugin]
---
<u>Context</u>:
During the migration of MINT to ```Ads```. We have observed that temporary file name clash can occur beetwen different applications.

<u>Description</u>:
To remove future potential name clash, we decided to specify a specific temporary directory for each application. For that purpose, we use the java system property ```java.io.tmpdir```.

The following files has been updated:
* ```server.sh```
* ```web.sh```
