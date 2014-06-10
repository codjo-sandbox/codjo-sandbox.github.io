---
layout: post
title: agf-gui-toolkit - Bug fix on Calendar validation
tags: [framework-1-126,codjo-gui-toolkit]
---
<u>Context</u>:
When an actionListener is added to a DateField, it is also added to the Calendar in order to validate the field when the user closes the calendar (See: [[framework:/2009/12/09/codjo-gui-toolkit - Bug fix on calendar validation]]). But it was impossible to remove this listener.

<u>Description</u>:
Method removeActionListener(ActionListener myActionListener) from DateField has been modified and now removes it as well.

See: [[framework:Utilisation de codjo-gui-toolkit]]