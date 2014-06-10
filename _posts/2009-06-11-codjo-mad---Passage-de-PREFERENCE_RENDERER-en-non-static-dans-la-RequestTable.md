---
layout: post
title: agf-mad - Passage de PREFERENCE_RENDERER en non-static dans la RequestTable
tags: [framework-1-100,codjo-mad]
---
Cet attribut est maintenant non-static car la même instance de ```DefaultTableCellRenderer``` (agrégée dans ```PreferenceRenderer```) était utilisée dans toutes les ```RequestTable```, ce qui posait des problèmes pour pouvoir utiliser une préférence dans la table de gauche dans le composant ```SelectionGui```