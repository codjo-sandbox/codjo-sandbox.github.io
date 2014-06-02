---
layout: post
title: maven-agf-plugin - Software projects can use idea-glue
tags: [framework-1-135,maven-codjo-plugin]
---
<u>Context</u>:
Working with ```damas```, idea glue didn't work.

<u>Description</u>:
```idea-glue``` has been modified to allow software projects like ```damas``` to make a glue with projects, libraries and/or plugins.

<u>Example</u>:
```
c:\dev\projects\framework\software\damas>idea -Dlib=referential,mad -Dappli=smart
```

see: [[framework:maven-codjo-plugin]]