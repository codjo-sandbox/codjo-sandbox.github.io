---
layout: post
title: agf-datagen - Ajout de la balise 'include-handler'
tags: [codjo-datagen,framework-1-37,hot-topics]
---
La balise ```include-handler``` permet d'ajouter tous les handlers d'une 'entity' filtrés par un pattern.
NB : Dans l'attribut 'entity', on spécifie un XPath.

<u>Exemple :</u>

Ajoute tous les handlers new et update des entités de type commençant par 'quarantine' :

```xml
<include-handler entity="/data/entity[[starts-with(@type,'quarantine')]]" 
                 pattern="(new|update)*"/>
```