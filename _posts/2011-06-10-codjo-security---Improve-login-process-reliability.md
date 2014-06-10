---
layout: post
title: agf-security - Improve login process reliability
tags: [framework-2-1,codjo-security,resolution-of-brin]
---
<u>Context</u>
It seems that in some very specific cases, the server login agent dies. Please see the BRIN [["Le batch de segmentation ne démarre pas"|http://wp-sic:8080/pyp/edit.html?id=0e1da8c1-8c16-4b47-b795-8e57944d2bb8]]

<u>Description</u>

In order to prevent the ```ServerLoginAgent``` death and therefore the inability to login, the appropriate behaviours are now wrapped using a ```thatNeverFails(...)``` technique (that catch all behaviour errors).
