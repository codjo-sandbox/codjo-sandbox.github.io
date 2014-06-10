---
layout: post
title: agf-datagen - Time is now logged when deleting data in audited tables
tags: [framework-1-172,codjo-datagen]
---
<u>Description</u>
Time was not logged when deleting data in tables being audited (using ```historic-audit-trail``` tag). Only the date was logged.

<u>Context</u>
The problem has been fixed.
