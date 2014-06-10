---
layout: post
title: agf-datagen - Gestion de famille de référentiels
tags: [codjo-datagen,framework-1-17]
---
\- Possibilité de définir pour chaque référentiel une liste de familles de référentiels auquel il appartient.
```
<entity name="com.agf.mint.ref.ExecutionVl" table="REF_EXECUTION_VL">
        <feature>
            <referential name="Référentiel VL d'exécution" familyList="MaFamille1, MaFamille2, etc"/>
        ...
        </feature>
...
</entity>
```
Fonctionnalité utilisée dans la librairie [[codjo-referential|http://wp-confluence/confluence/display/framework/agf-referential]].