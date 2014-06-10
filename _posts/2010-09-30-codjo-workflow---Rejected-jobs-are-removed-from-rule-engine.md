---
layout: post
title: agf-workflow - Rejected jobs are removed from rule engine
tags: [codjo-workflow,framework-1-169]
---
<u>Context</u>
Rejected jobs remained in the rule engine. This could block another ```Job``` if a rule prevented execution while the rejected job's type was present.

<u>Description</u>
Now rejected jobs are removed from the ```RuleEngine``` and a message is sent to the ```ScheduleLeaderAgent```.

See [[codjo-workflow - Writing rules for RuleEngine]]