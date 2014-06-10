---
layout: post
title: agf-mad - Fix in combo box sizing method
tags: [codjo-mad,framework-1-147,hot-topics]
---
<u>Context</u>:
The ```RequestComboBox.getPreferredSizeForContent()``` was used to properly set the width of combo box components, particularly in the filter panel and the quarantine windows, so that its largest item could be read entirely.

However the component's height was also modified to the maximum height for the current font. This did not take into account borders, margins and other look and feel characteristics.

<u>Description</u>:
Now the method uses the exact same height for the component, as computed by the Java platform.

See [[codjo-mad - Utilisation]]