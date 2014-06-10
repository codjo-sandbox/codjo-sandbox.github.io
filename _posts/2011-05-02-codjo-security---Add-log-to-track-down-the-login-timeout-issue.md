---
layout: post
title: agf-security - Add log to track down the login timeout issue
tags: [framework-1-196,codjo-security]
---
<u>Context</u>
On the Continuous integration server, we have a cyclic weird login time-out issue that blocked integration test. 

<u>Description</u>
Temporarily, the login agent will log all unexpected received message in the log file (client side, i.e. the SIC "sortie de la console" part). We hope that this log will help us to understand the issue.
