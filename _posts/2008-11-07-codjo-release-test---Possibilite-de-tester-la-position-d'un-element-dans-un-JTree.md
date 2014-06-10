---
layout: post
title: agf-release-test - Possibilité de tester la position d'un élément dans un JTree
tags: [framework-1-69,codjo-release-test]
---
La balise ```assertTree``` s'enrichit d'un nouvel attribut ```row``` permettant de vérifier la position d'un noeud dans l'arbre. Permet notamment de tester l'ordre des noeuds dans un arbre.

**{<u>}Exemple :</u>**
|| ![Alt attribute text Here](attachments/tree.jpg) || Par rapport à l'arbre ci-joint, les assertions suivantes sont vraies : \\
```
<assertTree name="Tree" path="rootName" exists="true" row="0"/>
<assertTree name="Tree" path="rootName:child1" exists="true" row="1"/>
<assertTree name="Tree" path="rootName:child1:child11" exists="true" row="2"/>
<assertTree name="Tree" path="rootName:child1:child11:child111" exists="true" row="3"/>
<assertTree name="Tree" path="rootName:child2" exists="true" row="4"/>
<assertTree name="Tree" path="rootName:child2:child21" exists="true" row="5"/>
``` ||
{info:title=Tip}
A noter que les assertions se font par rapport aux noeuds visibles à l'écran. Un élément présent dans l'arbre qui n'apparaitrait pas à l'écran à cause de noeuds repliés n'intervient pas dans le compte des lignes. Si nécessaire, afin de faciliter l'écriture des tests, la balise ```expandAllTree``` peut être utilisée pour déplier l'arbre complètement.
{info