---
layout: post
title: agf-test - Assertion d'un fichier Excel ouvert en TR
tags: [codjo-test,excel,tr,release,framework-1-44]
---
Ajout de la balise ```<assert-excel>``` qui permet de comparer un ficher ouvert dans excel avec un fichier excel étalon.
Il est obligatoire de passer les nombres de lignes et de colonnes à vérifier en attribut de la balise.

L'implémentation est basée sur jcom, et utilise une dll.

Exemple d'utilisation:
```
<gui-test>
    <group name="test de l'export excel">
        <click name="ExportExcelButton"/>
        <click name="SecuritiesTable" row="1" count="2"/>
        <selectTab name="tabbedPaneSecurity" tabLabel="FR0000031122"/>
    </group>
</gui-test>
<assert-excel expected="ExportXL_etalon.xls" columnCount="30" rowCount="15"/>
```
Voir la page : [[Assertion d'un fichier Excel ouvert en TR (configuration et utilisation)|codjo-release-test - Assertion d'un fichier Excel ouvert en TR]]