---
layout: post
title: agf-mad - Modification du format de communication client-serveur
tags: [framework-1-79,codjo-mad]
---
Déplacement des valeurs des attributs "value" des&nbsp;éléments "field" vers l'intérieur de l'élément.
\\

```title=AVANT
<field name="A" value="XXX"/>
```

```title=APRES
<field name="A">"XXX"</field>
```
Cette modification permet de corriger un défaut de performance du parser XML de Java utilisé côté serveur,&nbsp;lorsque la valeur des attributs est longue (~8 minutes pour une valeur de 300 ko, contre un parsing quasi-instantané).