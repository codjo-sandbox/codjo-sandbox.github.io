---
layout: post
title: agf-gui-toolkit - Ajout de nouvelles méthodes utilitaires dans la classe TreeUtil
tags: [framework-1-99,codjo-gui-toolkit]
---
** **getRenderedLabel(JTree, TreePath, TreeCellValueConverter)* renvoie le libellé rendu d'un noeud dont le chemin est passé en paramètre. Le _TreeCellValueConverter_ implémente la méthode _getValue(Component, Object)_ qui selon la complexité du composant _TreeCellRenderer_, renverra un libellé spécifique.
Exemple : 

```
 public static class IconCellValueConverter extends TreeCellValueConverter {
        @Override
        public String getValue(Component renderedComponent, Object modelObject) {
            IconTreeCellRenderer iconRenderer = (IconTreeCellRenderer) renderedComponent;

            Icon icon = iconRenderer.getIcon();
            return icon.getDescription() <u> " " </u>  modelObject.toString();

        }
}

```
** **getRenderedLabel(JTree, TreePath)* renvoie le libellé rendu d'un noeud dont le chemin est passé en paramètre et dont le TreeCellValueConverter est un _JLabelTreeCellValueConverter_ (En conséquence, le _TreeCellRender_ de l'arbre est obligatoirement un _JLabel_ (une exception _CastException_ est envoyé le cas échéant).
** **setSelectionPaths(JTree, TreePath[[]])* sélectionne un ensemble de chemins dans l'arbre
** **scrollSelectionToVisible(JTree tree, TreePath[[] newSelection, TreePath[]] oldSelection)* déplace le _ScrollPane_ de l'ancienne sélection vers la nouvelle.