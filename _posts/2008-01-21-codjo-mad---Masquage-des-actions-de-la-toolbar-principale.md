---
layout: post
title: agf-mad - Masquage des actions de la toolbar principale
tags: [codjo-mad,framework-1-27]
---
En fonction des droits utilisateurs, il est maintenant possible de masquer les boutons associées aux actions dans la toolbar principale.

Il suffit d'ajouter l'attribut **```hideWhenNotAllowed="true"```** dans la balise _component_ de type action du fichier _toolbar.xml_

Exemple:
```xml
<toolbar ... >
  ...
  <component action="MonAction" hideWhenNotAllowed="true" />
  <component plugin="MonPlugin" actionId="MonAutreAction" hideWhenNotAllowed="true" />
  ...
</toolbar>
```

Si l'utilisateur n'a pas le droit d'exécuter _MonAction_, le bouton correspondant ne sera pas visible sur la toolbar.

Par défaut, si l'attribut n'est pas spécifier, sa valeur est _false_.

De plus, les spérateurs superflus (sucessifs, ou situés en début/fin de toolbar) sont supprimés automatiquement.