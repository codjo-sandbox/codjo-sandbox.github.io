---
layout: post
title: agf-gui-toolkit - Amélioration de la cohérence de l'API sur NoNullDateField
tags: [codjo-gui-toolkit,framework-1-51]
---
La cohérence de l'API du composant ```NoNullDateField``` a été améliorée. Les notions d'```infiniteDate``` ont été retirées au profit de ```noNullDate```.

Voici la nouvelle API :
```xml
public class NoNullDateField extends DateField {

    public static final Date DEFAULT_NO_NULL_DATE = ...

    public Date getNoNullDate();

    public void setNoNullDate(Date newNoNullDate);

}
```