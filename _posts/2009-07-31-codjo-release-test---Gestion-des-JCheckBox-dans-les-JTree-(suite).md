---
layout: post
title: agf-release-test - Gestion des JCheckBox dans les JTree (suite)
tags: [hot-topics,framework-1-107,codjo-release-test]
---
Suite à l'[[évolution|/2009/01/08/codjo-release-test - Gestion des JCheckBox dans les JTree]] concernant les balises **select**, **editCell** et **assertTree**, la stratégie de recherche d'un noeud dans un JTree ne nécessite plus systématiquement de spécifier la valeur true/false du checkBox. Cette information n'est nécessaire que dans le cas de l'**assertTree**.

<u>Exemple</u>:
Avant on était obligé de spécifier l'état du ```JCheckBox``` lors d'un select. 
```
<select name="columnsTree" path="Tout [[false]:OPCVM [false]:Flag Hedgé [true]]"/>
```
Maintenant on peut écrire 
```
<select name="columnsTree" path="Tout:OPCVM:Flag Hedgé"/>
```
