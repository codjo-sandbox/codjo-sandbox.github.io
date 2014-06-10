---
layout: post
title: agf-segmentation -  Configuration d'un aspect
tags: [framework-1-96,codjo-segmentation]
---
La configuration d'un aspect a été adaptée au cas spécifique de la segmentation.

<u>Exemple de configuration</u>
```xml
<aspect id="SegmentationAspect" class="com.agf.oscar.SegmentationAspect">
    <description>
        Cet aspect se déclenche avant la segmentation (après le PRE du workflow de segmentation).
    </description>
    <join-points>
        <join-point call="after" point="segmentation.pre" />
    </join-points>
</aspect>
``` 