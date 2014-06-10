---
layout: post
title: agf-gui-toolkit - Possibilité de capturer la perte globale du focus d'un composant DateField
tags: [framework-1-108,codjo-gui-toolkit]
---
La classe ```DateFieldGlobalFocusValidator``` a été créée afin d'encapsuler le mécanisme permettant de déterminer si un DateField a dans sa globalité perdu le focus. 

<u>Exemple :</u>
```
// Construction
RestrictedDateField datefield = new RestrictedDateField();
DateFieldGlobalFocusValidator globalFocusValidator = new DateFieldGlobalFocusValidator(datefield);
datefield.setFocusValidator(globalFocusValidator);

// Pour détecter la perte de focus
globalFocusValidator.addFocusListener(new MyFocusListener());
```