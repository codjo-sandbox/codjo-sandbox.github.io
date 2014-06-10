---
layout: post
title: agf-control - Ajout flag de modification manuelle lors d'un forçage
tags: [codjo-control,framework-1-18]
---
Ajout d'une fonction ```isFormClean()```&nbsp;permettant de savoir si des modifications ont été effectuées&nbsp;ou non sur le formulaire par l'utilisateur lors du click sur le bouton "forcer" des écrans de détail des quarantaines.

Cette fonction permet&nbsp;de distinguer un comportements du bouton "forcer"&nbsp;distinct pour chacun des deux cas d'utilisations possibles (par ex : si les modifications doivent être prises en compte ou non).

Exemple :
```
public class MyQuarantineDetailWindow extends DefaultQuarantineDetailWindow {

    public MyQuarantineDetailWindow(DetailDataSource dataSource)
          throws RequestException {
        super(dataSource);
        dataSource.addDataSourceListener(new MyDataSourceListener());
    }

    private class MyDataSourceListener extends DataSourceAdapter {
        @Override
        public void beforeSaveEvent(DataSourceEvent event) {
           if (isFormClean()) {
                    /** un traitement **/
                }
                else {
                    /** un autre traitement **/
                }
          }
    }
}
```