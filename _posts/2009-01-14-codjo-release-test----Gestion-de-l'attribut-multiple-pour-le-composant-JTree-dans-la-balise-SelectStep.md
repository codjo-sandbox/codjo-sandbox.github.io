---
layout: post
title: agf-release-test -  Gestion de l'attribut multiple pour le composant JTree dans la balise SelectStep
tags: [framework-1-79,codjo-release-test]
---
L'attribut ```multiple``` de la balise <select> est à présent géré pour les JTree.
```
<select name="Tree" mode="model" path="root:Biere:Belge:Leffe"/>
<select name="Tree" mode="model" path="root:Vins:Francais:Sud-Ouest:Saint-Emilion" multiple="true"/>
```

Ainsi les noeuds Leffe et Saint-Emilion seront sélectionnés.