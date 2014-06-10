---
layout: post
title: agf-segmentation - Request identifier added to aspect context
tags: [codjo-segmentation,framework-1-119]
---
The aspect on segmentation process had no way to know the corresponding request identifier. The latter has been added to the context. The ```SegmentationAspectParticipant``` class has been modified accordingly.

```
public void run(AspectContext aspectContext) throws AspectException {
   SegmentationAspectContext context = new SegmentationAspectContext(aspectContext);
   [[...]]
   String requestId = context.getRequestId();
   [[...]]
}
```

See: [[aspect in codjo-segmentation]]