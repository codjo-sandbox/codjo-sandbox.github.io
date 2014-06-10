---
layout: post
title: agf-mad - Method FilterPanel.isRunning is now public
tags: [framework-2-11,codjo-mad]
---
<u>Context</u>
To avoid reloading the filters more than needed we have to know if filtering is running. A method exists in the API but with private visibility.

<u>Description</u>
The method ```isRunning()``` is now public.