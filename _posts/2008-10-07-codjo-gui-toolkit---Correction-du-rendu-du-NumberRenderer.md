---
layout: post
title: agf-gui-toolkit - Correction du rendu du NumberRenderer
tags: [framework-1-65,codjo-gui-toolkit]
---
La méthode ```format``` comparait la chaine ```"null"``` avec l'objet ```value```.

Dans certains cas particuliers, la chaine ```"null"``` n'était pas identifiée correctement.

On ajoute donc ```toString()``` dans le test ```if```.
```
private Object format(Object value) {
  if (format ![Alt attribute text Here](attachments/= null && value )= null && !"null".equals(value.toString())) { //modifié ici
    try {
      return format.format(new BigDecimal(value.toString()));
    }
    catch (Exception ex) {
      APP.error("Erreur lors du formatage de " + value);
    }
  }
  return value;
}
```