---
layout: post
title: agf-gui-toolkit - Contrôle extérieur du tooltip du DateField
tags: [codjo-gui-toolkit,framework-1-30]
---
Modifications du DateField pour permettre un contrôle du texte du tooltip par l'utilisateur de la lib.

Utile pour certaines applications qui n'ont pas forcément besoin d'afficher la valeur de la date saisie en tooltip mais un message personnalisé (rêgle de gestion concernant la date, par exemple).

<u>Exemple</u> :
```java
DateField d = new DateField();
d.setTooltipStandardMessageDisplayDateValue(false);
// A partir de ce moment là, le tooltip affichera bien le message précisé ci-dessous
// et non la date sélectionnée dans le composant.

d.setTooltipStandardMessage("Cette date doit être inférieure à la date du jour.");
...
```