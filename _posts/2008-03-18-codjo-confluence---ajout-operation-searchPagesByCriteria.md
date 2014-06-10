---
layout: post
title: agf-confluence - ajout opération searchPagesByCriteria
tags: [codjo-confluence,framework-1-35]
---
Cette méthode accepte comme paramètre un objet de Type ```SearchCriteria```

Exemple :

```
SearchCriteria criteria = new DefaultSearchCriteria();
criteria.withCriteria("auteur", "toto")
        .withCriteria("document", "AAAM")
        .withRangeCriteria("date", "20080101", "20080115");

List<Page> list = 
   operations.searchPagesByCriteria(SPACE_KEY, criteria, 50);

```