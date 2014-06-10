---
layout: post
title: agf-mad - Modification ButtonPanelGui et ButtonPanelLogic
tags: [codjo-mad,framework-1-27]
---
La visibilité de certaines méthodes de ces 2 classes est passée de private à protected afin de pouvoir modifier le comportement du bouton Valider et Annuler.

Une classe dérivant de ButtonPanelLogic a été créée dans Mint et a surchargé certaines méthodes pour pouvoir valider et annuler une saisie sans fermer l'écran (l'annulation entraînant le rechargement de la datasource principale et datasources filles éventuellement). Pour fermer l'écran, un bouton 'Fermer' a été ajouté dans une classe dérivant de ButtonPanelGui.
\\
\\