---
layout: post
title: agf-reflect - Ajout de la classe PreloadClassesMainWrapper
tags: [framework-1-84,codjo-reflect]
---
Une classe ```PreloadClassesMainWrapper``` permettant de forcer le chargement des classes en mémoire a été ajoutée. Elle est nécessaire pour le mécanisme de calcul de la couverture de code par les tests-release.

<u>Exemple</u>

Le code suivant permet de :
1. charger toutes les classes contenues dans le package ```com.agf.mypackage``` (ainsi que dans les sous-packages).
1. appeler la méthode ```main``` de la classe ```MyMain``` avec les arguments ```arg1``` et ```arg2```.

```
PreloadClassesMainWrapper.main(new String[[]]{"com.agf.mypackage",
                                            "com.agf.mypackage.MyMain", "arg1", "arg2"})
```