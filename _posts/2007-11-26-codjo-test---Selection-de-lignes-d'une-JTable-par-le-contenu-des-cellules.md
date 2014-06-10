---
layout: post
title: agf-test - Sélection de lignes d'une JTable par le contenu des cellules
tags: [codjo-test,framework-1-21]
---
Il devient possible de sélectionner une ligne d'une JTable en fonction du contenu des cellules.

Exemple :
```
<select name="nomJTable" label="libellé"/>
```

Sélectionnera la ligne dont une des cellules contient "libellé". Si plusieurs lignes correspondent, ou si aucune ligne n'est trouvée, le step renvoie une erreur.