---
layout: post
title: agf-release-test - Vérification de contenu html
tags: [framework-1-76,codjo-release-test]
---
La balise ```assertValue``` permet maintenant de tester le contenu d'un ```JEditorPane``` configuré en  ```text/html```.

Il est possible de vérifier le texte affiché :
```xml
    <assertValue name="messageEditor" expected="Texte en gras"/>
```

ainsi que le html correspondant :
```xml
    <assertValue name="messageEditor" expected="<b>Texte en gras</b>" mode="model"/>
```
