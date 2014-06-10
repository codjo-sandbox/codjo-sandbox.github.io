---
layout: post
title: agf-release-test - Ajout de la balise AssertTab
tags: [framework-1-79,codjo-release-test]
---
Une balise assertTab a été ajoutée afin de vérifier la présence d'un onglet dans un JTabbedPane.

Exemple de sélection d'un onglet par son label :
```
<assertTab name="monTabbedPane" tabLabel="Titre de l'onglet"/>
```

Exemple de vérification par le label et l'index :
```
<assertTab name="monTabbedPane" tabLabel="Titre de l'onglet" tabIndex="0"/>
```
Dans ce dernier cas, on vérifie que l'onglet existe et est positionné au bon index.