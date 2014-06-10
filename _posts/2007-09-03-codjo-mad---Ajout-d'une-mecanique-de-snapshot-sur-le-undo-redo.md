---
layout: post
title: agf-mad - Ajout d'une mécanique de snapshot sur le undo-redo
tags: [codjo-mad,framework-1-10]
---
Dans certains cas, certaines opérations effectuées sur le GUI provoquent le calcul et la mise à jour de plusieurs champs GUI déclarés dans les DataSource. Du coup, dans la gestion du undo/redo, celà conduit à un comportement incohérent puisque l'utilisateur se retrouve à effectuer des opérations "undo" sur des actions GUI qui n'ont pas été effectuées par ses soins.
&nbsp;
Pour remédier à ce problème une mécanique de "snapshot" a été mise en place dans la gestion du undo/redo afin de regrouper plusieurs actions unitaires sur le GUI en une seule unité.
&nbsp;
Dans l'exemple suivant, le fait de cliquer sur&nbsp;la checkbox provoque la mise à jour&nbsp;d'un composant JTextField et d'un composant DateField.
&nbsp;
```
checkBox.addItemListener(new ItemListener() {
    public void itemStateChanged(ItemEvent event) {
        if (checkBox.isSelected()) {
            buttonPanelLogic.startSnapshotMode();
            textField.setText("OK");
            dateField.setDate(java.sql.Date.valueOf("2007-08-24"));
            buttonPanelLogic.stopSnapshotMode();
        }
    }
});
```\\
\\
\\

La mise à jour des deux composants est encapsulée par des appels aux méthodes "startSnapshotMode()" et "stopSnapshotMode()" qui vont créer une seule unité "undo/redo".

Du coup, lorsque l'utilisateur va cliquer sur la checkbox, les deux composants vont être mis à jour d'un coup puis lors du clic sur "undo", l'utilisateur va revenir d'un coup à l'état précédent (checkbox décliquée, remise à la valeur précédente des deux composants JTextField et DateField).