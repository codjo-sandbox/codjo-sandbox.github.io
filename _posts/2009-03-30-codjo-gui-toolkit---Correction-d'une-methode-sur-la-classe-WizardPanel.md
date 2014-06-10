---
layout: post
title: agf-gui-toolkit - Correction d'une méthode sur la classe WizardPanel
tags: [framework-1-89,codjo-gui-toolkit]
---
<u>Problème</u>
L'exécution de certains tests release liés à l'assistant d'import/export a mis en évidence 1 bug dans la classe ```WizardPanel```. Dans la méthode _repaintPanel(Step)_, le panel était vidé de ses composants puis reconstruit. Le problème est que Swing tente de re-valider le panel à chaque ajout de composant ce qui peut entraîner des exceptions.

<u>Solution</u>
- La méthode _invalidate()_ a donc été invoquée en début de méthode afin que Swing ne tente pas de re-valider le panel en pleine "reconstruction".
- Le corps de la méthode _propertyChange_ du ```StepPanelUpdater``` a été mis dans un thread Swing