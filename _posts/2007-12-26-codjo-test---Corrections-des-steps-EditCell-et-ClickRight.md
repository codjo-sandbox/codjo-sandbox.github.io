---
layout: post
title: agf-test - Corrections des steps EditCell et ClickRight
tags: [codjo-test,framework-1-25]
---
Dans les steps EditCell et ClickRight, il n'était pas possible de tester des composants dont le nom était utilisé dans d'autres composants en dehors du contexte. Exemple avec un écran qui pourraient comporter ces 2 tables ayant la même structure :
{panel:title=Gestion des Frais| borderStyle=dashed| borderColor=#ccc| titleBGColor=#F7D6C1| bgColor=#FFFFCE}
**Frais Directs :&nbsp;**
|| dénomination || montant HT \\ || montant TTC \\ ||
| CAC | 10.45 | 15.75 |
&nbsp;**Frais Indirects :**
|| dénomination || montant HT \\ || montant TTC \\ ||
| COUIC | 12.44 | 17.85 |
{panel}
On veut asserter la valeur du montant la ligne COUIC de la table des frais indirects. Jusqu'ici, le finder JFCUnit pouvait trouver plusieurs composants car il effectuait une recherche globale à l'IHM et l'assertion ne passait pas.

A présent, le finder effectuera sa recherche depuis le composant qui a été placé dans le contexte de la step EditCell ou ClickRight