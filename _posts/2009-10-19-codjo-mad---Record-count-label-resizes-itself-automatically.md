---
layout: post
title: agf-mad - Record count label resizes itself automatically
tags: [framework-1-118,codjo-mad]
---
The ```RequestRecordCountField``` did not appropriatly resize itself when its text was updated.

Now the component uses font metrics to change its preferred size if needed.

![Alt attribute text Here](attachments/requestrecordcountfield1.PNG)