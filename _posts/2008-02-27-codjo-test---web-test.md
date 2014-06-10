---
layout: post
title: agf-test - web-test
tags: [codjo-test,framework-1-33]
---
- balise ```<EditForm>``` : ajout de l'attribut ```position``` qui permet de récupérer le formulaire d'après sa position dans une page web. Il ne sera pris en compte que si l'attribut ```id``` n'est pas spécifié
- balise ```<AssertTable>``` : idem

Exemple:
```xml
<editForm position="2">
...
</editForm>
```
- possibilité de désactiver javascript dans la balise ```<web-test>```. Par défaut, javascript est activé.

Exemple:
```xml
<web-test session="maSession" url="www.monsite.com" javascript="false">
...
</web-test>
```