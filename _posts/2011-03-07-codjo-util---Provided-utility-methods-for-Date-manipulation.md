---
layout: post
title: agf-util - Provided utility methods for Date manipulation
tags: [framework-1-190,codjo-util]
---
<u>Context</u>
Utility methods for Date manipulation have been found in Mint application.

<u>Description</u>
These utility methods are not Mint-specific. It has been decided to move them into ```codjo-util```. Here is the API of the ```DateUtil``` class:

```
public static String getUSCurrentDate();
public static Date getCurrentDate();
public static String getUSDate(Date date);
public static String getUSDate(long millis);
public static String getUSDate(String date);
public static String getTimestampDate(Date date);
public static String getFrenchDate(Date date);

public static Date parseUSDate(String date);
public static Date parseFrenchDate(String date);
public static Date parseTimestampDate(String date);

public static String shiftUSDate(String dateToShift, int nbOfDays);
public static Date shiftDate(Date dateToShift, int nbOfDays);
public static boolean hasDateChanged(Date oldDate, String newDate);
public static int getYear(Date date);
```

see [[codjo-util - Utilisation|http://wp-confluence/confluence/display/framework/agf-util<u>-</u>Utilisation]]