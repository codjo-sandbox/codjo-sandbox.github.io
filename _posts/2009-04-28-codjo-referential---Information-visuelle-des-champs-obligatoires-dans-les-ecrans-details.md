---
layout: post
title: agf-referential - Information visuelle des champs obligatoires dans les écrans détails
tags: [codjo-referential,framework-1-93,hot-topics]
---
Une icône apparaît par défaut à côté des champs requis dans les écrans détails. Un ToolTip spécifie aussi que le champ est obligatoire.
Pour afficher les icônes associées aux champs requis, nous utilisons le composant ```FeedbackPanel``` de codjo-gui-toolkit.

![Alt attribute text Here](attachments/requiredFields.JPG)

Si ces champs ne sont pas remplis, il est désormais impossible de valider l'écran détail. Pour cela, le ```RequiredFieldsValidator``` est branché par défaut.