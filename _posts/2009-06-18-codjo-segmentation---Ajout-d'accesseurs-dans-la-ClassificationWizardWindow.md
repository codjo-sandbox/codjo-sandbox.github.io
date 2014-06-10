---
layout: post
title: agf-segmentation - Ajout d'accesseurs dans la ClassificationWizardWindow
tags: [framework-1-101,codjo-segmentation]
---
Des accesseurs sur le panneau principal et la&nbsp;table de classification&nbsp;de l'assistant de segmentation ont été ajoutés :
```java
    public LabelledItemPanel getMainPanel() {
        return classificationStep.mainPanel;
    }

    public RequestTable getClassificationTable() {
        return classificationStep.getClassificationTable();
    }
```

\\
&nbsp;\\