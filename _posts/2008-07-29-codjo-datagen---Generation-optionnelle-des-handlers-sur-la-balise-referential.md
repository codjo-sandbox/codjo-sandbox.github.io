---
layout: post
title: agf-datagen - Génération optionnelle des handlers sur la balise referential
tags: [codjo-datagen,framework-1-51]
---
L'attribut ```generateHandler``` a été ajouté à la balise ```referential``` (la valeur par défaut est ```true```). Cette balise permet de ne pas générer automatiquement les handlers associés aux besoins de la gestion de référentiel. Cela permet notamment de les personnaliser avec des requêtes spécifiques.

<u>Exemple</u> : Pour ne pas générer les handlers, il suffit d'écrire la ligne suivante.
```xml
<referential generateHandler="false"/>
```
