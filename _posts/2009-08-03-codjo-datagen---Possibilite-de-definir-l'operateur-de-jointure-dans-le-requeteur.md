---
layout: post
title: agf-datagen - Possibilité de définir l'opérateur de jointure dans le requêteur
tags: [hot-topics,framework-1-107,codjo-datagen]
---
Dans le requêteur, la clé de jointure était précédemment définie par une ou plusieurs égalité(s) entre 2 champs.

<u>Exemple</u> :
Avant
```
<entity ... table="TABLE_SOURCE">
   <feature ...>
     <handler-requetor id="alltranscoRaiSecurity">
          <link to="TABLE_DESTINATION">
              <key from="INSTR_ID" to="INSTR_ID"/>
           </link>
     </handler-requetor>
```
Maintenant, l'utilisateur peut préciser l'opérateur.
```
<entity ... table="TABLE_SOURCE">
   <feature ...>
     <handler-requetor id="alltranscoRaiSecurity">
          <link to="TABLE_DESTINATION">
              <!--  "TABLE_SOURCE.INSTR_ID <= TABLE_DESTINATION.INSTR_ID" -->
              <key from="INSTR_ID" to="INSTR_ID" operator="&lt;=" /> 
           </link>
     </handler-requetor>
```