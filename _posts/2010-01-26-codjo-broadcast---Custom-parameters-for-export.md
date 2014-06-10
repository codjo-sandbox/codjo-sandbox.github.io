---
layout: post
title: agf-broadcast - Custom parameters for export
tags: [framework-1-131,codjo-broadcast,hot-topics]
---
<u>Context</u>:
Mint application needs specific arguments for some export. Some development ([[codjo-plugin - Custom parameters in export.ksh|framework:/2009/12/14/agf-plugin - Custom parameters in export.ksh]]) has been done for that but only mandatory arguments (user name, broadcast file and broadcast date) were sent to Vtom.

<u>Description</u>:
The ```BroadcastVtomCaller``` now uses each argument (including optional ones) set in every single ```StepPanel``` of the wizard (through a call to ```setValue``` method) to generate the command line sent to Vtom. Moreover, every argument is displayed on the wizard summary screen.

<u>Example</u>:
In Mint, the optional argument _"linkTypeCode"_ is set with value _"REPORTING"_ through a customized ```StepPanel``` of the wizard.

The summary screen looks like:
![Alt attribute text Here](attachments/broadcast.jpg)

The generated command line is:
_userName ALLPERF.txt 2010-01-26 \-linkTypeCode REPORTING_