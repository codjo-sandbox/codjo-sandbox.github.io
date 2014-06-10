---
layout: post
title: agf-segmentation - Exception message is changed on SegmentationAspectParticipant
tags: [framework-1-151,codjo-segmentation]
---
<u>Context</u>:
The catch block in ```SegmentationAspectParticipant.transactionalPointCreate(JobRequest, JobAudit)``` gave the exception's message directly to a ```StringBuilder``` constructor. This constructor throws a ```NullPointerException``` if the given parameter is ```null```.

<u>Description</u>:
If the exception message is ```null```, the exception class name is used instead.

See [[Documentation codjo-segmentation]]