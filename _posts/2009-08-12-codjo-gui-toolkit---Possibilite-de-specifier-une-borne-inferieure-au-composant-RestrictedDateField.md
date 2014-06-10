---
layout: post
title: agf-gui-toolkit - Possibilité de spécifier une borne inférieure au composant RestrictedDateField
tags: [framework-1-107,codjo-gui-toolkit]
---
La news est obsolète car la fonctionnalité à été enrichie ici [[/2009/08/06/codjo-gui-toolkit - Possibilité de définir un intervalle de dates à exclure par le composant RestrictedDateField]]

Avec le composant RestrictedDateField, il est maintenant possible, dans le cas où l'on veut bloquer la saisie de dates dans le passé, de spécifier la date maximum du passé.

<u>Exemple</u> :
```
// on autorise la saisie de dates dans le passé  :
RestrictedDateField dateField = new RestrictedDateField(true, true);

// on n'autorise PAS la saisie de dates dans le passé  :
dateField = new RestrictedDateField(false, true);

// on n'autorise pas la saisie de dates antérieures au 31/12/2010 (inclus) :
Calendar cal = Calendar.getInstance();
cal.set(Calendar.YEAR, 2010);
cal.set(Calendar.MONTH, Calendar.DECEMBER);
cal.set(Calendar.DAY_OF_MONTH, 31);
dateField.setMaxPastDate(cal.getTime());
```