---
layout: post
title: agf-mad - Ajout d'un nouveau mode de filtrage dynamique BD pour les écrans liste
tags: [framework-1-111,hot-topics,codjo-mad]
---
Un nouveau mode d'utilisation a été implémenté dans la classe ```FilterPanel```. Dans ce mode, il n'y a plus de bouton "Afficher" et le filtrage de la ```RequestTable``` est déclenché lors de la sélection d'une valeur dans un filtre de type ```RequestComboBox``` ou la perte de focus sur un filtre de type ```JTextField```.

Pour construire un ```FilterPanel``` fonctionnant dans ce mode, il faut utiliser l'un des deux constructeurs suivant en mettant ```false``` sur le dernier paramètre :
```
public FilterPanel(RequestTable requestTable, boolean hasSearchButton)

public FilterPanel(RequestTable requestTable, final WaitingPanel waitingPanel, boolean hasSearchButton)
```
