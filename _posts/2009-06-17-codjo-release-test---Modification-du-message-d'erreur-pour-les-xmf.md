---
layout: post
title: agf-release-test - Modification du message d'erreur pour les xmf
tags: [framework-1-100,codjo-release-test]
---
Il était souvent laborieux d'identifier quel groupe d'un test-release plantait lorsque le test release faisait appel à plusieurs fichiers xmf.

Désormais, le message d'erreur généré par un test plantant dans un .xmf a été modifié de telle sorte que le nom du fichier .xmf apparait en préfixe du nom du groupe dans lequel le test a planté. Le nom du fichier est séparé du nom du groupe par ':::'

Exemple:
```
Global.xml:80: Step 1 du groupe '../LigneALigne.xmf:::Test du Ligne à Ligne A' (SelectTabStep)
```
Dans cette exemple Global.xml fait appel à plusieurs xmf, dont LigneALigne.xmf