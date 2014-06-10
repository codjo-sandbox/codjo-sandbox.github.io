---
layout: post
title: agf-release-test - Bug dans la balise closeFrame
tags: [framework-1-88,codjo-release-test]
---
La balise ```closeFrame``` ne simulait pas correctement la fermeture des ```JInternalFrames```.

Avant, certains tests étaient écrits de cette manière :
```xml
<assertFrame title="Première fenêtre"/>
...
<assertFrame title="Deuxième fenêtre"/>

<closeFrame title="Première fenêtre"/>
<click name="deuxiemeFrame.calcul" count="2"/> <![Alt attribute text Here](attachments/-- count==2 sinon ça ne marchait pas )![Alt attribute text Here](attachments/) -->
```

Maintenant, on peut les écrire normalement comme suit :
```xml
<assertFrame title="Première fenêtre"/>
...
<assertFrame title="Deuxième fenêtre"/>

<closeFrame title="Première fenêtre"/>
<click name="deuxiemeFrame.calcul"/>
```
