---
layout: post
title: agf-gui-toolkit - Ajout du composant DateFieldWithDateRestriction
tags: [framework-1-53,codjo-gui-toolkit]
---
Création d'un nouveau composant ```DateFieldWithDateRestriction``` héritant de ```DateField``` et offrant la possibilité d'interdire la saisie :
* d'une liste de dates
* des dates passées
* des week-end

{info} chacune des fonctionnalités ci-dessus est débrayable individuellement{info}

Ces conditions sont envoyées au JCalendar, les dates interdites sont alors grisées et leur sélection est impossible