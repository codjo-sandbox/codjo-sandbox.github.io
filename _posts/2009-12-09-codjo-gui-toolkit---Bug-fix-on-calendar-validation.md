---
layout: post
title: agf-gui-toolkit - Bug fix on calendar validation
tags: [framework-1-125,codjo-gui-toolkit]
---
<u>Context</u>: 
```DateField``` accepts ```ActionListeners``` to trigger an action when the content is validated. When the calendar was used, clicking the ok button didn't call these listeners and so didn't validate the data.

<u>Description</u>: 
It has been corrected. Now, when the calendar closes, it triggers the events to the ```DateField``` and calls its listeners.

See: [[codjo-gui-toolkit]]
