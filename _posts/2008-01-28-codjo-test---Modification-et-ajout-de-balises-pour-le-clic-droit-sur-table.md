---
layout: post
title: agf-test - Modification et ajout de balises pour le clic droit sur table
tags: [codjo-test,framework-1-28]
---
**Modification de la balise ```<clickRight>```** pour permettre la saisie du paramètre ```column```. Si non renseigné, ce paramètre vaut 0 par défaut. La valeur du paramètre peut soit être l'index de la colonne désirée soit son entête.

**Ajout de la balise ```<clickRightTableHeader>```.** A l'instar de la balise ```<clickRight>```, cette balise permet de simuler un clic droit sur l'entête d'une table. La syntaxe et l'utilisation est similaire à la balise ```<clickRight>```.

Exemple :
```
<clickRightTableHeader name="maTable" column="0">
    <assertListSize expected="2"/>
    <assertList row="0" expected="Supprimer" />
    <assertList row="1" expected="Filtrer"/>
    <assertEnabled menu="Supprimer" expected="true"/>
    <assertEnabled menu="Filtrer" expected="true"/>
</clickRightTableHeader>
```\\