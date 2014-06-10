---
layout: post
title: agf-release-test - Indépendance vis à vis du TreeNode
tags: [framework-1-80,codjo-release-test]
---
Modification du code de l'editCellStep de façon à être indépendant du type du model.

Avant :
```
TreeNode node = (TreeNode)treePath.getLastPathComponent();
return tree.getCellEditor().getTreeCellEditorComponent(tree, node, true, tree.isExpanded(treePath),node.isLeaf(), tree.getRowForPath(treePath));
```
Après :
```
Object node = treePath.getLastPathComponent();
boolean isLeaf = tree.getModel().isLeaf(node);
boolean expanded = tree.isExpanded(treePath);
int pathRow = tree.getRowForPath(treePath);
return tree.getCellEditor().getTreeCellEditorComponent(tree, node, true, expanded, isLeaf, pathRow);

```