---
layout: post
title: agf-gui-toolkit - Paramétrage de la date infinie dans NoNullDateField
tags: [codjo-gui-toolkit,framework-1-46]
---
Dans la classe ```NoNullDateField```, il est maintenant possible de changer la date infinie via la méthode ```setInifiniteDate```.

<u>Exemple</u> :

```java
Date infiniteDate = 
    new GregorianCalendar(8888, Calendar.FEBRUARY, 5).getTime();
NoNullDateField dateField = new NoNullDateField();
dateField.setInfiniteDate(infiniteDate);
```