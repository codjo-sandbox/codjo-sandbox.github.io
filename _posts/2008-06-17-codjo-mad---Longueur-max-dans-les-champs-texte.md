---
layout: post
title: agf-mad - Longueur max dans les champs texte
tags: [codjo-mad,framework-1-49]
---
Suite à la [[modification|/2008/04/17/codjo-mad - Modification du DetailDataSource]] permettant de renseigner automatiquement la taille max des ```JTextComponent``` et des ```NumberField``` liés à des ```DetailDataSource```, un bug a été corrigé : si la précision n'était pas renseignée dans ```Structure.xml```, une longueur max de zéro était mise en place.
Après correction, la longueur max n'est plus modifiée.