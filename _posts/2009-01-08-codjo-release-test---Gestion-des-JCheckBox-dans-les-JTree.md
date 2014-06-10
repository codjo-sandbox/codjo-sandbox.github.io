---
layout: post
title: agf-release-test - Gestion des JCheckBox dans les JTree
tags: [framework-1-78,codjo-release-test]
---
Les balises **select, editCell**&nbsp;et **assertTree** peuvent désormais&nbsp;gérer l'état d'un JCheckBox dans un JTree.
Chaque noeud spécifie son état "activé/désactivé" via les mots-clefs "false/true" entre crochets.

Exemple d'**assertTree** :
```
<assertTree name="columnsTree" path="Tout [[false]:Bond [false]:Next Call [false]]" exists="true"/>
```
Exemple de **select** :
```
<select name="columnsTree" path="Tout [[false]:OPCVM [false]:Flag Hedgé [true]]"/>
```
Exemple d'**editCell**:
```
<editCell name="columnsTree" path="Tout [[false]:OPCVM [false]:Flag Hedgé [true]]"/>
	<click/>
</editCell>
```\\