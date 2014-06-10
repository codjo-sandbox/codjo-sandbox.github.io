---
layout: post
title: agf-referential - Bug fix in RelatedFieldValueUpdater class
tags: [framework-1-149,codjo-referential]
---
<u>Context :</u>
For DAMAS project, a system based on master-slaves fields was asked. But there was an anomaly with numerical fields.

<u>Description :</u>
There was an anomaly in the class whose responsability was to update numerical slave fields values from the master one.
By now, it's fixed.