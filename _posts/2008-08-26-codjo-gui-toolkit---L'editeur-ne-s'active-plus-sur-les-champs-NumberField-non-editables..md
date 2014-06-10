---
layout: post
title: agf-gui-toolkit - L'éditeur ne s'active plus sur les champs NumberField non editables.
tags: [framework-1-58,codjo-gui-toolkit]
---
Auparavant les champs nombres (```NumberField```) se plaçaient en mode édition au focus sans tenir compte de l'attribut ```isEditable```. Ceci est maintenant corrigé, ce qui permet d'obtenir des champs sélectionnables mais non modifiables.