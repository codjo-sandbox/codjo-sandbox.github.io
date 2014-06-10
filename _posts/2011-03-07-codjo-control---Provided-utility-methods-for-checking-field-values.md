---
layout: post
title: agf-control - Provided utility methods for checking field values
tags: [framework-1-190,codjo-control]
---
<u>Context</u>
Utility methods for checking field values during control steps have been found in Mint application.

<u>Description</u>
These utility methods are not Mint-specific. It has been decided to move them into ```codjo-control```. Here is the API of the ```ControlUtils``` class:

```
public static void checkFieldNotNull(Object fieldValue, int errorNumber, String field);
public static void checkFieldNotBlank(String fieldValue, int errorNumber, String field);
public static void checkFieldStrictlyGreaterThanThreshold(BigDecimal fieldValue,
                                                          double threshold,
                                                          int errorNumber,
                                                          String errorMessage);
public static void checkFieldStrictlyInsideBounds(BigDecimal fieldValue,
                                                  double minThreshold,
                                                  double maxThreshold,
                                                  int errorNumber,
                                                  String errorMessage);
public static void checkFirstValueLowerThanSecondValue(BigDecimal firstValue, 
                                                       BigDecimal secondValue,
                                                       int errorNumber,
                                                       String errorMessage);
public static void checkFirstDateNotNullIfSecondDateNotNull(Date firstDate,
                                                            Date secondDate,
                                                            String firstDateName,
                                                            String secondDateName,
                                                            int errorCode);
public static void checkSecondDateAfterFirstDate(Date firstDate,
                                                 Date secondDate,
                                                 String firstDateName,
                                                 String secondDateName,
                                                 int errorCode);
public static void checkDateInsideBounds(Date beginDate, Date shiftDate, Date endDate);
```