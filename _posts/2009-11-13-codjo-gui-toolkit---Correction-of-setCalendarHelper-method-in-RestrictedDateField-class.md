---
layout: post
title: agf-gui-toolkit - Correction of setCalendarHelper method in RestrictedDateField class
tags: [framework-1-122,codjo-gui-toolkit]
---
<u>Context</u> 
In the ```RestrictedDateField``` class, the method ```setCalendarHelper(CalendarHelper)``` is an override of the setter method defined in the class ```AbstractDateField```.
It should set the field ```calendarHelper``` and redefine its renderer. 
But, it never set the field.

<u>Description</u>
Now, the method set correctly the field.
