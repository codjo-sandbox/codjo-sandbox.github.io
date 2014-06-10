---
layout: post
title: agf-gui-toolkit - Création de TreeUtil et TableUtil
tags: [codjo-gui-toolkit,framework-1-26]
---
Deux classes utilitaires ont été créées :
** **TreeUtil* : classe utilitaire pour les JTree. Voilà son interface
void expandSubtree(JTree tree, TreePath path) : permet d'ouvrir les noeuds d'un JTree pour un chemin donné.
boolean isLeaf(JTree tree, TreePath path) : permet de savoir si un TreePath correspond à un noeud fils.

** **TableUtil* : classe utilitaire pour les JTables. Elle permet de synchroniser les largeurs de différentes JTables, synchroniser les Viewport de différentes JTables, forcer l'arrêt de l'édition d'une JTable, ajouter un PropertyChangeListener écoutant le redimmensionnement des colonnes d'une table.
