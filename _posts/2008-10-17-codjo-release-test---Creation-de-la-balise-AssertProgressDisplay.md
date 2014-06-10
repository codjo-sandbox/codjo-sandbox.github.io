---
layout: post
title: agf-release-test - Création de la balise AssertProgressDisplay
tags: [framework-1-66,codjo-release-test]
---
Cette nouvelle balise permet de tester l'affichage momentané d'un composant dans le glass pane d'une fenêtre (```JDialog```, ```JFrame```, ```JWindow``` ou ```JInternalFrame```).

Elle prend un attribut ```name``` correspondant au nom du composant visé.

Exemple :
```
...
<clickButon label="Lancer traitement"/>
<assertProgressDisplay name="waitingPanel"/>
...
```

[[Doc|codjo-release-test - Tags IHM#assertProgressDisplay]]