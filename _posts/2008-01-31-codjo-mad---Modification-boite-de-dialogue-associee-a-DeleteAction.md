---
layout: post
title: agf-mad - Modification boîte de dialogue associée à DeleteAction
tags: [codjo-mad,framework-1-29]
---
Le libellé des boutons de la boîte de dialogue ouverte suite à une suppression de ligne sur une RequestTable a évolué : les boutons **OK** et **Annuler** ont été remplacés par des boutons **Oui** et **Non**.

Cette évolution est un impact de la correction faite sur codjo-test concernant le click label. En effet, dans certains tests, il y avait ambiguïté entre les libellés **Annuler** d'une boîte de dialogue et de la frame parent.

Il y aura un impact sur certains tests-release. Il faudra les modifier en prenant en compte le nouveau nom des boutons de la boîte de dialogue de la manière suivante :
- remplacer **<click label="OK"/>** relatives à l'ouverture d'une boîte de dialogue par **<click label="Oui"/>**
- remplacer **<click label="Annuler"/>** relatives à l'ouverture d'une boîte de dialogue par **<click label="Non"/>**