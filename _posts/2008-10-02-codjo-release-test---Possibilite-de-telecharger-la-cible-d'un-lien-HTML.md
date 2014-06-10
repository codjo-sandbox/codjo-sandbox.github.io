---
layout: post
title: agf-release-test - Possibilité de télécharger la cible d'un lien HTML
tags: [framework-1-64,codjo-release-test]
---
La nouvelle balise ```downloadFile``` permet de télécharger la cible d'un lien dans un fichier.
Attributs :
* link : texte du lien
* target : nom du fichier cible

Exemple :
```
<web-test ...>
   ...
   <downloadFile link="Export Excel" target="export.xls"/>
   ...
</web-test>
```

Doc : [[codjo-release-test - Tags web#downloadFile]]