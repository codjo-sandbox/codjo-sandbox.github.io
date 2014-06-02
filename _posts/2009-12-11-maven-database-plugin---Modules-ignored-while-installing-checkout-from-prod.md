---
layout: post
title: maven-database-plugin - Modules ignored while installing checkout from prod
tags: [framework-1-126,maven-database-plugin,resolution-of-brin]
---
<u>Context</u>:
{info:title=Resolution of BRIN}
To solve the BRIN "Resource data-test unavailable", ```InitFromProdMojo``` had to manually configure modules which were to be ignored during install of the checkout from prod.
{info}

<u>Description</u>:
Following modules are now ignored :
** \**-batch
** \**-gui
** \**-client
** \**-server
** \**-common
** \**-release-test

see: [[codjo-maven-common - Resolution of BRIN "Resource data-test unavailable"|framework:/2009/12/10/agf-maven-common - Resolution of BRIN "Resource data-test unavailable"]]