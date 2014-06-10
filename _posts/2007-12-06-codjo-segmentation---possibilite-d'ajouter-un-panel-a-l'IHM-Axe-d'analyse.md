---
layout: post
title: agf-segmentation - possibilité d'ajouter un panel à l'IHM Axe d'analyse
tags: [framework-1-23,codjo-segmentation]
---
Il est désormais possible de remplacer le panel qui contient les champs cutomizés par un panel donné dans l'IHM Axe d'analyse.

Pour cela, au lieu d'utiliser la méthode 'addClassificationExtensionField' (pour ajouter des composants), il faut appeler la méthode 
```setClassificationExtensionPanel(JPanel panel)```

Exemple :
```
    private static class ClassificationSettingsCustomizerWithMyPanel implements SegmentationSettingsCustomizer {

        public void doPreDataSourceInit(ClassificationStructureLogic structureLogic,
                                        DetailDataSource dataSource)
              throws RequestException {

             JPanel jPanel = new JPanel();
             JTextField field = new JTextField(10);
             jPanel.add(field);

             structureLogic.getGui().setClassificationExtensionPanel(jPanel);
        }

        public void doPostDataSourceInit(ClassificationStructureLogic structureLogic,
                                         DetailDataSource dataSource)
              throws RequestException {

        }
    }
```