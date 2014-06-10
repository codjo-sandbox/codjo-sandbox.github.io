---
layout: post
title: agf-test - La balise editCell gère maintenant les arbres
tags: [codjo-test,framework-1-28]
---
On peut à présent se servir de la balise **editCell** pour éditer un **JTree**. Le chemin du noeud à éditer est précisé de la même façon que pour la balise **select**, en utilisant ':' pour séparer les différents éléments du chemin. Ce chemin peut être spécifié en utilisant le modèle de l'arbre (**mode='model'**) ou le renderer de l'arbre (**mode='display'**). Le mode par défaut est de type 'display'.

Dans l'exemple suivant, l'éditeur de l'arbre renvoie un **JPanel** contenant un bouton "Editer". Le test suivant permet de cliquer sur ce bouton.

Exemple :
```
<editCell name="monArbre" path="root:noeudA:noeudB">
    <click label="Editer"/>
    ...
</editCell>
```\\