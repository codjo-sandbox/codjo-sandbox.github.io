---
layout: post
title: agf-imports - Line number available in filtering expressions
tags: [framework-1-126,codjo-imports,hot-topics]
---
<u>Context</u>
When importing files via ```codjo-imports``` library, it is possible to reject some lines according to some expressions. Until now, "Valeur", which is the line to be imported was the only variable available to build the expression.

<u>Description</u>
A new variable "NumLigne", which is the line number in the imported file, can be used to build the expression.

<u>Example</u>
```
NumLigne < 5 || Valeur.startsWith("XXXXXXXXXX")
```