---
layout: post
title: agf-test - Les balises editCell peuvent maintenant être imbriquées
tags: [codjo-test,framework-1-28]
---
Ce besoin nous est apparu dans le cas d'une table dont certaines cellules devaient contenir un JTree lui-même éditable (chaque noeud faisait apparaitre un bouton d'édition des valeurs du noeud).

Exemple :
```
<editCell name="maTable" row="3" column="Statut">
    <editCell path="root:noeud1">
        <click name="editButton"/>
        <setValue name="combo" value="VALEUR2"/>
        <click label="OK"/>
    </editCell>
</editCell>
```\\