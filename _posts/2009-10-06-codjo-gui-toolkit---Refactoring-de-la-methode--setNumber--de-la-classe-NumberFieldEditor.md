---
layout: post
title: agf-gui-toolkit - Refactoring de la méthode "setNumber" de la classe NumberFieldEditor
tags: [framework-1-116,codjo-gui-toolkit]
---
Auparavant la méthode ```setNumber(Object value)``` de la classe ```NumberFieldEditor``` ne prenait en compte que le cas où le paramètre était une chaine de caractères. 
Dorénavant, cette méthode accepte aussi les paramètres de type ```Number```.