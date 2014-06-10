---
layout: post
title: agf-segmentation - Segmentation engine enhancement
tags: [codjo-segmentation,framework-1-143,hot-topics]
---
<u>Context</u>:
Some Oscar users encountered a problem when creating axes containing a lot of sleeves.
The latter were concatenated in a table column and could grow beyond ```varchar``` limits.

see: [[swdev:Reunion architecture du 20100408 - Segmentation]]


<u>Description</u>:
This database storage has been replaced with a dynamic string construction.