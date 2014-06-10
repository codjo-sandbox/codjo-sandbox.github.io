---
layout: post
title: agf-broadcast - Customisation du Wizard d'export
tags: [framework-1-6,codjo-broadcast]
---
Il est maintenant possible de personnaliser l'assistant d'export en ajoutant des étapes.

Il suffit de passer par la configuration du plugin ```BroadcastGuiPlugin```

```java
BroadcastGuiPlugin guiPlugin = ....

guiPlugin.getConfiguration()
         .setBroadcastWizardCustomizer(new BroadcastWizardCustomizer() {
  public void customizeWizard(Wizard wizard) {
     wizard.addStep(new SelectPeriodStep());
  }
});
```
