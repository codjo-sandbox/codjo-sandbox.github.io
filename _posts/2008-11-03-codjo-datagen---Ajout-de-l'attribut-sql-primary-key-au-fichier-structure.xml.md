---
layout: post
title: agf-datagen - Ajout de l'attribut sql-primary-key au fichier structure.xml
tags: [framework-1-69,codjo-datagen]
---
Un nouvel attribut a été ajouté à l'élément ```<field/>``` de ```structure.xml```. Il indique si le champ fait partie de la clé primaire.

Exemple de fichier généré :
```
<structure>
    <table ...>
        <field ... sql-primary-key="true"/>
    </table>
    ...
</structure>
```