---
layout: post
title: agf-release-test - Renvoi d'une erreur en cas de tentative de clic sur un menu désactivé
tags: [framework-1-63,codjo-release-test]
---
Cliquer sur un menu désactivé (balise ```click```) renvoie maintenant une erreur. Auparavant la balise ne faisait rien dans ce cas.

Exemple si Ouvrir est grisé :
```<click menu="Fichier:Ouvrir"/>```
A l'exécution :
```Step N du groupe 'X' (ClickStep) 
--> Menu désactivé : Ouvrir```