---
layout: post
title: agf-release-test - Exécution de gui-test dans différentes sessions
tags: [codjo-release-test,framework-1-58]
---
Suite à [[l'évolution de la balise gui-test|/2008/06/26/codjo-test - Execution de plusieurs gui-test dans une même session]] précédente, la notion de ```session``` a été remaniée.
Il est maintenant possible de lancer plusieurs instances de ```GUI```, chacune étant identifiée par une ```session```.

<u>Exemple</u> : deux instances de GUI différentes
```xml
<gui-test session="sessionDeBarbara">
   <!-- Barbara consulte le referentiel des produits -->
</gui-test>

...

<gui-test session="sessionDeBrandon">
   <!-- Brandon met à jour le referentiel des produits -->
</gui-test>

...

<gui-test session="sessionDeBarbara">
   <!-- Barbara rafraichit et constate la mise à jour du referentiel -->
</gui-test>
```