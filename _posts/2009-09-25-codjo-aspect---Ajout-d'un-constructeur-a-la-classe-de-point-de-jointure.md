---
layout: post
title: agf-aspect - Ajout d'un constructeur à la classe de point de jointure
tags: [framework-1-115,codjo-aspect]
---
Un constructeur avec paramètres a été rajouté à la classe ```JoinPoint```. Il permet d'initialiser directement toutes les propriétés de la classe.

```
public JoinPoint(int call, String point, String argument)
```

De plus, un contrôle a été ajouté sur la propriété ```call``` pour vérifier qu'elle a bien une des trois valeurs définies en constante dans la classe :
<table>
<tr>
<th>Constante</th><th>Valeur numérique</th></tr>
<tr>
<td> ```CALL_BEFORE``` </td>
<td> 1 </td>
</tr>
<tr>
<td> ```CALL_AFTER```  </td>
<td> 2 </td>
</tr>
</table>
| ```CALL_ERROR```  | 3 