---
layout: post
title: agf-mad - Ajout composant FilterableRequestComboBox
tags: [codjo-mad,framework-1-47]
---
Un nouveau composant graphique de type ```ComboBox```, dérivant de la classe ```RequestComboBox```, a été ajouté. Il permet à l'utilisateur de filtrer la liste d'éléments sélectionnables dans la combo en fonction de la saisie au clavier de l'utilisateur:

ex:

Soit une combo avec 3 choix possibles :

b
ab
abc

Lorsque l'utilisateur sélectionne la combo et appuie sur les touches 'a' puis 'b', les choix possibles dans la combo sont restreints à 'ab' et 'abc'. 