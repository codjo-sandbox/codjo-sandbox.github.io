---
layout: post
title: Add-exec-methods-with-command-array-on-WindowsExec
tags: [codjo-util, framework-2-56]
---
## Context
A deadlock sometimes happened while doing these steps in an application :
1 - clic on menu Audit > Logs (workflow logs)
2 - clic on menu Audit > Server administration

## Description
The deadlock has been fixed by managing GUI lock/unlock in the Event Dispatch Thread (which removes the need of synchronization).