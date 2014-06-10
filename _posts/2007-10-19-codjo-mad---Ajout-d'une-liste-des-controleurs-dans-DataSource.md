---
layout: post
title: agf-mad - Ajout d'une liste des contrôleurs dans DataSource
tags: [codjo-mad,framework-1-17]
---
Afin vérifier si on peut sauvegarder une data source.
Très utile quand on veut enchaîner différentes vérifications avant la sauvegarde sans passer par un property change.

Ex:

```
...
// on ajout le contrôle dans la data source
myDataSource.addController(new MyController());
...

private class MyController implements DataSource.Controller {
  // cette méthode va être appelé juste avant la sauvegarde de la data source
  public boolean control() {
    return getText() > 15; // si vrai, on sauvegarde, si faux on ne sauvegarde pas
  }
}
```