---
layout: post
title: agf-plugin - Better management of file encoding in scripts
tags: [framework-1-125,codjo-plugin]
---
<u>Context</u>:
File encoding configuration was inconsistent between development and integration servers. In development, it was by default ```windows-1252``` and in integration, it was set to ```ISO-8859-1```.
This incoherence implied bad euro character management.

<u>Description</u>:
```server.sh```, ```web.sh```, ```export.ksh``` and ```import.ksh``` have been modified to set file encoding to ```windows-1252```.