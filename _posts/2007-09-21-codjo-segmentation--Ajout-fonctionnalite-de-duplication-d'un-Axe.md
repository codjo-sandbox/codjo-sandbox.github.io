---
layout: post
title: agf-segmentation- Ajout fonctionnalité de duplication d'un Axe
tags: [codjo-segmentation,framework-1-13]
---
Il est désormais possible de dupliquer le paramétrage d'un axe de segmentation dans l'IHM de paramétrage des axe(Boutton + Menu contextuel).

L'axe est recopié dans son intégralité, les poches de cet axe seront identiques aux poches de l'axe d'origine etc.

La seule valeur modifiée est le nom de l'axe :&nbsp;**Copie** ($NEW_AXIS_ID$) **de** $OLD_AXIS_NAME$

**Important** :

Pensez à mettre à jour les applications utilisant la librairie de segmentation : Dans les 3 fichiers _livraison-sql.txt_, _grant.sql_ et _revoke.sql_ penser à prendre en compte&nbsp;la procédure stockée _sp_SEG_Copy_AxisClassification_