---
layout: post
title: agf-tokio - Mise en place d'un mécanisme de localisation des lignes
tags: [framework-1-112,codjo-tokio,hot-topics]
---
Un mécanisme de localisation des lignes a été mis en place.

Les messages d'erreurs produits lors d'insertions de ```tokio``` ou lors de comparaisons d'étalons affichent désormais la localisation de la ligne à l'origine du problème.

Prochainement, ce mécanisme sera utilisé par le ```tokio-viewer``` et permettra à partir d'une ligne de retrouver son origine dans les fichiers tokio.

<u>Exemple</u> : erreur lors de la comparaison des lignes
```
[[tokio-set-db]] Chargement du scenario AddIssuer
[[tokio-assert]] Verification de toutes les tables
Erreur à la ligne suivante :
row - AddIssuer.tokio:144
   row - AddIssuer.tokio:23

[[Comparator]] Ligne 1 table AP_ISSUER en erreur ![Alt attribute text Here](attachments/)!
   expected :[ISSUER_NAME=12 SPV SA, ISSUER_CODE=MADELE, SPV_FLAG=N, ...
   valeur   :{ISSUER_NAME=12 SPV SA, ISSUER_CODE=MADELE, SPV_FLAG=N, ...

	[[ISSUER_TYPE]]	expected = (OPCVM)	valeur   = (STANDARD)
	[[NAME_UPDATE_DATE]]	expected = (2005-04-20 00:00:00.0)	valeur   = (null)
	[[ID_BB_COMPANY]]	expected = (B2000)	valeur   = (A1000)
```
