---
layout: post
title: agf-gui-toolkit - Possibilité de définir un intervalle de dates à exclure par le composant RestrictedDateField
tags: [framework-1-108,codjo-gui-toolkit,hot-topics]
---
Il est maintenant possible de définir des intervalles de dates à exclure dans le composant ```RestrictedDateField``` de la manière suivante :

<u>Exemple :</u>

```
// les dates exclues sont dans l'intervalle [[MIN_DATE - maxDate]], soit les dates inférieures à maxDate
dateField.setMaxDateRange(maxDate); 

// les dates exclues sont dans l'intervalle [[minDate - MAX_DATE]], soit les dates supérieures à minDate
dateField.setMinDateRange(minDate); 

// définit l'intervalle de dates exclues
dateField.addInvalidRange(minDate, maxDate); 
```