---
layout: post
title: agf-release-test - La balise assertTab permet de tester si un onglet est sélectionné
tags: [framework-1-88,codjo-release-test]
---
La balise ```assertTab``` a été enrichie d'un attribut ```selected``` permettant de tester si un onglet est sélectionné ou pas. Cet attribut est optionnel.

<u>Exemple</u>
```
<selectTab name="tabbedPaneDetail" tabLabel="Cours"/>
<assertTab name="tabbedPaneDetail" tabLabel="Cours" selected="true"/>
```