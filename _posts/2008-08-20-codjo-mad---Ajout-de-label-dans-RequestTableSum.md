---
layout: post
title: agf-mad - Ajout de label dans RequestTableSum
tags: [framework-1-58,codjo-mad]
---
Ajout de la possibilité d'insérer du texte dans la ligne de total ```RequestTableSum``` pour les colonnes qui ne sont pas "summable"

**preference.xml :**
```
<preference id="prefId">
        [[..]]
        <column fieldName="field0" summableLabel="TOTAL"/>
        <column fieldName="field1" summable="true" />
        [[..]]
</preference>
```
{note:title=Attention}
summableLabel et summable ne peuvent pas être utilisés sur une même colonne.
{note}