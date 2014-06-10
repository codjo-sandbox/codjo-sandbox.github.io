---
layout: post
title: agf-gui-toolkit - Coordination des filtres de type Combo sur les tables
tags: [codjo-gui-toolkit,framework-1-52]
---
Une classe ```TableFilterComboGroup``` s'occupe à présent de coordonner les ```TableFilterCombo``` par rapport à la table filtrée. Cette fonctionnalité prend tout son sens dans le cas où les combos sont configurées en ```autoApply``` à ```false```.

Exemple d'utilisation :
```
TableFilter tableFilter = new TableFilter(model);
jTable.setModel(tableFilter);

TableFilterCombo comboColA = new TableFilterCombo(tableFilter, 0);
TableFilterCombo comboColB = new TableFilterCombo(tableFilter, 1);
comboColA.setAutoApplyFilter(false);
comboColB.setAutoApplyFilter(false);

TableFilterComboGroup group = new TableFilterComboGroup();
group.add(comboColA);
group.add(comboColB);

comboColA.setSelectedItem("1");
comboColB.setSelectedItem("A");
group.applyFilter();
```