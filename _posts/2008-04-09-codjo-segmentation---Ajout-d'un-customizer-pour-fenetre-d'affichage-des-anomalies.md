---
layout: post
title: agf-segmentation - Ajout d'un customizer pour fenêtre d'affichage des anomalies
tags: [framework-1-39,codjo-segmentation]
---
Ajout d'un customizer pour fenêtre d'affichage des anomalies

Ex de customizer :

```
public class MyAnomalyLogWindowCustomizer implements AnomalyLogWindowCustomizer {
  public void customizeWindow(LogWindowLogic anomalyLogWindowLogic) {
	anomalyLogWindowLogic.getGui().getTable()
                  .setCellRenderer("sleeveCode", new MySimpleTableCellRenderer());
  }
}
```
Configuration du plugin :
```
plugin.getConfiguration().setAnomalyLogWindowCustomizer(new MyAnomalyLogWindowCustomizer());
```