---
layout: post
title: agf-segmentation - Modification de la gestion du requeteur pour l'affichage des résultats
tags: [framework-1-17,codjo-segmentation]
---
Il est désormais possible d'utiliser à la fois le requeteur et des champs de tables liées dans la liste d'affichage des résultats.

La syntaxe du&nbsp;fichier ```segmentation-configs.xml``` change toutefois un peu :
```xml
<result-config>
    <requetor>allSegmentationResults</requetor>
    <where-clause>(SEGMENTATION_RESULT.ANOMALY=$anomaly$ or $anomaly$ =-1)
        and SEGMENTATION_RESULT.CLASSIFICATION_ID = $segmentationId$
        and (SEGMENTATION_RESULT.MY_KEY='$myKey$' or '$myKey$'='')
    </where-clause>
    <join-key left="SEGMENTATION_RESULT" type="inner" right="LINKED_TABLE">
        <part left="MY_KEY" operator="=" right="MY_KEY"/>
    </join-key>
    <column label="Ma clé" value="MY_KEY" table="SEGMENTATION_RESULT"/>
    <column label="Libellé lié" value="MY_KEY_LABEL" table="LINKED_TABLE"/>
</result-config>
```
Dans la balise ```<column>``` on précise maintenant uniquement le nom du champ concerné au format SQL dans l'attribut ```value```. Dans l'attribut ```table``` (obligatoire) on précise le nom de la table d'ou provient ce champ au format SQL également.

On peut désormais dans la balise <```result-config>``` utiliser à la fois un ```<requetor>``` et des ```<join-key>```. {warning:title=Attention}Il est indispensable de penser à mettre à jour les fichiers ```segmentation-configs.xml``` dans les applications. {warning} Pensez à consulter la [[Documentation codjo-segmentation]].
\\
\\
\\
\\ \\