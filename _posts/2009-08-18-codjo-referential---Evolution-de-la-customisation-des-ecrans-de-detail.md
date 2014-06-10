---
layout: post
title: agf-referential - Evolution de la customisation des écrans de détail
tags: [framework-1-109,codjo-referential]
---
Lorsqu'une ```ReferentialDetailLogic``` utilisait un ```GuiCustomizer```, les composants de type ```RequestComboBox``` non customisés n'étaient pas initialisés.

Maintenant: 
 - L'initialisation des combobox customisées est laissée à la charge du customizer. 
 - L'initialisation des autres combobox est effectuée par la librairie.