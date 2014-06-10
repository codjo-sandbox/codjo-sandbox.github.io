---
layout: post
title: agf-control - Remove attribute syncValidation and display Waiting Panel
tags: [framework-2-17,codjo-control]
---
<u>Context</u>
For ```Roses``` some actions in quarantine GUI are very long and the user doesn't know when action is finished.

<u>Description</u>
The Waiting Panel has been added on ```DeleteAction```, ```SendAction```, ```ValidateAction``` and  ```ForceAction```.
A refactoring has been realised , the attribute ```syncValidation``` has been removed but the behaviour of this attribute has become the default behaviour.