---
layout: post
title: agf-segmentation - Possibilité d'ajouter un aspect
tags: [framework-1-93,codjo-segmentation]
---
Il est maintenant possible d'ajouter un aspect à un traitement de segmentation.

```xml|title=MySegmentationAspect.xml
<aspect id="SegmentationAspect" class="com.agf.oscar.SegmentationAspect">
    <description>
        Cet aspect se déclenche lors de la segmentation.
    </description>
    <join-points>
        <join-point call="after" point="segmentation" argument=""/>
    </join-points>
</aspect>
```