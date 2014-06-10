---
layout: post
title: agf-reflect - Possibilité d'exclure des packages dans PreloadClassesMainWrapper
tags: [framework-1-86,codjo-reflect]
---
Un nouvel argument "-exclude" est disponible sur la classe ```PreloadClassesMainWrapper``` pour exclure du chargement un ou plusieurs packages (les packages à exclure doivent être séparés par des ';').

<u>Exemple</u>

Le code suivant permet de charger toutes les classes contenues dans le package ```com.agf.mypackage``` (ainsi que dans les sous-packages), à l'exception des packages ```com.agf.mypackage.exclude1``` et ```com.agf.mypackage.exclude2```.

```
PreloadClassesMainWrapper.main(new String[[]]{"com.agf.mypackage",
                                            "-exclude",
                                            "com.agf.mypackage.exclude1;com.agf.mypackage.exclude2"
                                            "com.agf.mypackage.MyMain", "arg1", "arg2"})
```