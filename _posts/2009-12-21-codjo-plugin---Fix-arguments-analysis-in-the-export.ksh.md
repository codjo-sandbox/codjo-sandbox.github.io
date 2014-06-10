---
layout: post
title: agf-plugin - Fix arguments analysis in the export.ksh
tags: [framework-1-127,codjo-plugin]
---
<u>Context</u>:
In the latest modification of the export.ksh (see this [[news|http://wp-confluence/confluence/display/framework/2009/12/14/codjo-plugin<u>-</u>Custom<u>parameters</u>in+export.ksh]]), there was a bug in the arguments analysis so the release tests of the exports which use custom parameters were not able to succeed in the remote context.

<u>Description</u>:
This bug was fixed.