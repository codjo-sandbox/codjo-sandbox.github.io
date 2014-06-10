---
layout: post
title: maven-database-plugin - Accept different OS end of line characters for script execution
tags: [framework-2-21,maven-database-plugin]
---
<u>Context</u>
The build of the segmentation library fails because its procedure order file contains unix end of line and the plugin doesn't split the content of the file as expected.

<u>Description</u>
Now the plugin accepts different OS end of line characters for script execution.
