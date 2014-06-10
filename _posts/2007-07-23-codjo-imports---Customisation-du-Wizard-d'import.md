---
layout: post
title: agf-imports - Customisation du Wizard d'import
tags: [framework-1-6,codjo-imports]
---
Il est maintenant possible de personnaliser l'assistant d'import en ajoutant des étapes.

Il suffit de passer par la configuration du plugin ```ImportsGuiPlugin```

```java
ImportsGuiPluginguiPlugin = ....

guiPlugin.getConfiguration()
         .setImportsWizardCustomizer(new ImportsWizardCustomizer() {
  public void customizeWizard(Wizard wizard) {
     wizard.setPreFinalStepAction(new PreFinalStepAction() {...} );
  }
});
```
