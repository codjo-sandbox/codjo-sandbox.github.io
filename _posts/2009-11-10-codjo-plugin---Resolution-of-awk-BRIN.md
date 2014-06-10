---
layout: post
title: agf-plugin - Resolution of awk BRIN
tags: [framework-1-121,codjo-plugin,hot-topics,resolution-of-brin]
---
{info}Resolution of BRIN{info}

<u>Context</u>: 
Servers were not correctly stopped because of the following error:
```awk: record `mntexdev  1339  0.2 ...' too long.```

<u>Description</u>: 
In ```server.sh``` and ```web.sh``` scripts, calls to ```awk``` have been replaced by calls to ```gawk``` which accepts longer strings.