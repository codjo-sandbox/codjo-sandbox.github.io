---
layout: post
title: agf-mad - Suppression de la méthode deprecated initRequestComboBox
tags: [framework-1-26,codjo-mad]
---
Utiliser plutôt la méthode non statique :

```public void initRequestComboBox(String, String, boolean)```

Pas de références dans projets Maven 2 pour la méthode supprimée (seulement ProjetPims utilise toujours cette méthode).