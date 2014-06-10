---
layout: post
title: agf-pom - Ajout de joda-time
tags: [framework-1-53,codjo-pom,hot-topics]
---
La librairie [[joda-time|http://wp-confluence/confluence/display/dsi/Joda-Time]] a été ajoutée au super-pom. C'est une librairie permettant de manipuler des dates et heures. Pour l'utiliser , ajouter ceci dans votre fichier pom.xml : 
```
<dependency>
    <groupId>joda-time</groupId>
    <artifactId>joda-time</artifactId>
</dependency>
```

Exemples d'utilisation :
```java

DateTime currentDate = new DateTime();

//Lundi de la semaine précédente
DateTime firstDate = currentDate.minusWeeks(1).withDayOfWeek(DateTimeConstants.MONDAY);

Interval interval = new Interval(firstDate, new DateTime(2009, 01, 01, 0, 0, 0, 0));
if (interval.contains(currentDate)) {
     System.out.println("le " <u> currentDate.dayOfWeek().getAsText() </u> " " +
                                currentDate.getDayOfMonth() <u> "/"</u>
                                currentDate.getMonthOfYear()<u>"/" </u>
                                currentDate.getYearOfEra())+ " est dans la période";
  }
```

