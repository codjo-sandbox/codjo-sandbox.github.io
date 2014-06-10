---
layout: post
title: agf-gui-toolkit - Refactoring sur RestrictedDateField
tags: [framework-1-113,codjo-gui-toolkit]
---
2 méthodes ont été ajoutées:
```
public boolean containsExcludedDate(Date value)
```
Cette méthode retourne vrai si la date passée en paramètre est contenue dans un des intervalles de date à exclure.

```
public void clearExcludedDateRanges()
```
Cette méthode supprime tous les intervalles de date à exclure.
