---
layout: post
title: agf-referential - Changement de visibilité des classes ReferentialGui et ReferentialForm
tags: [framework-1-71,codjo-referential]
---
Pour les besoins d'un développement qui a été ensuite annulé, les classes ```ReferentialGui``` et  ```ReferentialLogic``` avaient été modifiées afin d'être visible hors de leur "package" (voir [[/2008/10/21/codjo-referential - Classes ReferentialGui et ReferentialLogic rendues publiques]]). 
Le besoin n'étant plus d'actualité, ces classes ne sont dorénavant visibles que par les objets de leur package.
