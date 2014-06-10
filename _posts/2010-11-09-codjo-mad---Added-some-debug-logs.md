---
layout: post
title: agf-mad - Added some debug logs
tags: [codjo-mad,framework-1-173]
---
<u>Context</u>
When the user clicks on the "Export to Excel" button in the MAD toolbar, there is no tracing of the action except for some very specific error cases.

<u>Description</u>
Some of the action's methods and data are now logged in level DEBUG.

See [[codjo-mad - Utilisation]]