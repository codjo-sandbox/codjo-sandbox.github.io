---
layout: post
title: agf-datagen - Historic audit now works on QUser table
tags: [framework-1-164,codjo-datagen]
---
<u>Context</u>:

When the ```historic-audit-trail``` xml tag was used on the Quarantine table definition, data audit didn't work on the associated ```QUser``` table.

<u>Description</u>:
Now the ```historic-audit-trail``` tag affects also the ```QUser``` table associated with the quarantine table.