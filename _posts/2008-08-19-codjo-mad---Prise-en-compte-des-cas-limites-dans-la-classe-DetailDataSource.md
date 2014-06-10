---
layout: post
title: agf-mad - Prise en compte des cas limites dans la classe DetailDataSource
tags: [framework-1-58,codjo-mad]
---
Modification de la méthode ```updateGuiFieldsForSave``` afin de prendre en compte le cas où le résultat serait null lors d'un save du ```DataSource```.

Voici le code de la méthode modifiée
```
private void updateGuiFieldsForSave(Result result) {
        // Si résultat null ou vide
        if (result == null || result.getRowCount() == 0) {
            return;
        }
        ....
    }
```