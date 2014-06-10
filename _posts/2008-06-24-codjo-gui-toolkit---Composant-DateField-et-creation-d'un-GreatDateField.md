---
layout: post
title: agf-gui-toolkit - Composant DateField et création d'un GreatDateField
tags: [framework-1-49,codjo-gui-toolkit]
---
Amélioration du composant DateField :
* Lorsqu'on change de mois ou d'année, le premier jour du mois est sélectionné par défaut
* Dans la combo des années, il y a désormais une scrollbar (stockage de 500 dates)

Création du composant GreatDateField :
* La date est saisissable dans un seul JTextField
* La fenêtre du calendrier s'ouvre lorsqu'on clique dans le JTextField de la date
* 5 boutons ont été ajoutés en dessous du calendrier : <u> 1 an, </u> 2 ans, ..., + 5 ans : ils permettent de sauter d'1, 2, 3, 4 ou 5 ans à partir de la date sélectionnée.

Impression Ecran : ![Alt attribute text Here](attachments/greatCalendar.JPG|thumbnail,align=center)