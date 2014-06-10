---
layout: post
title: agf-tokio - Amélioration des balises include-story
tags: [codjo-tokio,framework-1-38]
---
Dans les fichiers ```cases```, la balise ```include-story``` permet l'inclusion de fichiers à partir d'un chemin relatif.
Il est maintenant possible de lui fournir une ressource accessible depuis le ```ClassLoader```.

* Exemple :
```xml
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE cases PUBLIC "-//AGF, Inc.//DTD stories 2.0//EN" "cases.dtd">
<cases>
    <case id="NominalCase">
        <include-story file="/test/cases/referentialWithInput.tokio"/>
...
```