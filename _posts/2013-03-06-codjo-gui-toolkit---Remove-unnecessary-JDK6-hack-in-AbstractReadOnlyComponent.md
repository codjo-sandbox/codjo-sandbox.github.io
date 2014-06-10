---
layout: post
title: agf-gui-toolkit - Remove unnecessary JDK6 hack in AbstractReadOnlyComponent
tags: [framework-2-43,codjo-gui-toolkit]
---
<u>Context</u>
Mint release tests were KO since July 2012 because some components were sometimes not initialised with correct read only properties.

<u>Description</u>
see : https://github.com/codjo/codjo-gui-toolkit/pull/11