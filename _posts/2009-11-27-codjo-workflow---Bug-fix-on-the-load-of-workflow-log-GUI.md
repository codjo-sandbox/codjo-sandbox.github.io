---
layout: post
title: agf-workflow - Bug fix on the load of workflow log GUI
tags: [framework-1-124,codjo-workflow]
---
<u>Context</u>:
When we close the workflow Log GUI and lines displayed are filtered and we open again the GUI, the displayed lines are the same that previous display whereas filter is reset.
The previous selector on the ```RequestTable``` is used again at the GUI opening.

<u>Description</u>:
We use the method apply() of ```TableFilterPanel``` to load the table with a new selector.
