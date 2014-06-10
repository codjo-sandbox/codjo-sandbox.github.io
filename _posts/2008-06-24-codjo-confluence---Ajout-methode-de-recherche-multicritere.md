---
layout: post
title: agf-confluence - Ajout méthode de recherche multicritère
tags: [codjo-confluence,framework-1-49]
---
La méthode ```searchByCriteria``` dans la classe ```ConfluencePlugin``` a été ajoutée.
Contrairement à la méthode ```searchPagesByCriteria```, cette méthode renvoie les résultats de recherche (```SearchResult```) et non les pages (```Page```) correspondant aux résultats.

```
public List<SearchResult> searchByCriteria(String spaceKey, 
                                           SearchCriteria criteria, 
                                           int maxResults)
                          throws ConfluenceException
```