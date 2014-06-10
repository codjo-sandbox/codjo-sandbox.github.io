---
layout: post
title: agf-segmentation - Ajout d'un point d'exécution pour un aspect après traitement
tags: [framework-1-115,codjo-segmentation]
---
Un aspect peut être déclenché après le traitement de la segmentation (cf. [[documentation|http://wp-confluence/confluence/x/sRS9]]).

La configuration de l'aspect sera faite de la façon suivante :
```
<join-points>
    <join-point call="after" point="segmentation.post"/>
</join-points>
```

Un contexte spécifique a été créé ```SegmentationAspectContext``` avec les propriétés "connection", "arguments" et "audit".
```
protected void doRun(AspectContext context) {
    SegmentationAspectContext segmentationContext = new SegmentationAspectContext(context);
    [[...]]
    Connection connection = segmentationContext.getConnection();
    Arguments arguments = segmentationContext.getArguments();
    JobAudit audit = segmentationContext.getAudit();
    [[...]]
}
```