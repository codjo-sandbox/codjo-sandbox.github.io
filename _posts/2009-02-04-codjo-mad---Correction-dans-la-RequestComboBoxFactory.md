---
layout: post
title: agf-mad - Correction dans la RequestComboBoxFactory
tags: [framework-1-82,codjo-mad]
---
Correction sur la création d'une requestCombobox par la méthode suivante :
```
createRequestCombobox(String handlerId,String keyColName,String labelColName,boolean containsNull)                                                                                                                                                                       
```

Le modèle de la combobox était alimenté par le paramètre ```labelColName```, maintenant il est alimenté par ```keyColName```.

