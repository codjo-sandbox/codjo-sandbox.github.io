---
layout: post
title: agf-mad (ajout composants pour tables croisées)
tags: [framework-1-7,codjo-mad]
---
* Ajout&nbsp;d'une fonctionnalité&nbsp;de tri dans la classe ```RequestCrossTablePanel```
**** Ajout de&nbsp;la classe ```RequestCrossTableRendererSorter```, et&nbsp;instantiation par défaut de cette classe dans ```RequestCrossTablePanel```
\\
\\
* Ajout d'un composant permettant une somme en ligne pour une table croisée
**** Création de la classe&nbsp;```RequestCrossTableSum``` (et de sa classe de test)
**** Exemple d'utilisation dans **Gabi** : ```com.agf.mad.gui.request.CrossTableWithSumPanel```
\\
\\