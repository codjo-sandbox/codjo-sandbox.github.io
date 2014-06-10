---
layout: post
title: agf-test - Comparaison de fichier excel
tags: [codjo-test,framework-1-30]
---
La balise [[file-assert]] a été modifié pour supporter la comparaison de fichier excel. 

Cette stratégie de comparaison est activée lorsque les fichiers à comparer se terminent avec l'extension 'xls'

<u>Exemple</u>
```xml
<file-assert expected="etalon.xls" actual="result.xls"/> 
```

**NB** : Pour rappel, le fichier ```result.xls``` doit se trouver dans le répertoire pointé par la variable ```broadcast.output.dir```.
