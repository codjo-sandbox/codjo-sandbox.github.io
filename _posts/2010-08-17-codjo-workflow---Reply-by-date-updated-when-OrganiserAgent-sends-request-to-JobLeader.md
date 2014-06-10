---
layout: post
title: agf-workflow - Reply-by date updated when OrganiserAgent sends request to JobLeader
tags: [codjo-workflow,framework-1-160,resolution-of-brin]
---
{info}Resolution of BRIN{info}

<u>Context</u>
When a new ```JobRequest``` is sent to the ```OrganiserAgent```, the 'Reply-by' date is initialised by the ```ScheduleLeaderAgent```.

The ```JobLeaderBehaviour``` checks the 'Reply-by' date against the current date, and throws an error if it is older.

Since a ```JobRequest``` is withheld (not sent) while the job is in ```WAITING``` status in the rule engine, this 'Reply-by' date can expire. The following message appears in the ```TaskManager```:

![Alt attribute text Here](attachments/Sans titre.bmp)

<u>Description</u>
When the ```OrganiserAgent``` sends the ```JobRequest``` message to the ```JobLeaderBehaviour```, it overwrites the 'Reply-by' date.

See [[codjo-workflow - Parallelisation]]