---
layout: post
title: agf-mad - Modification des methodes setSecurityFunction et isEnabled de AbstractGuiAction
tags: [codjo-mad,framework-1-45]
---
Certains tests release de Mint liés à la gestion des droits plantaient aléatoirement sur le test de l'état 'Actif/Non Actif de composants dérivant de AbstractGuiAction. 2 méthodes ont été modifiées :
- isEnabled qui prend en compte dans la condition le droit d'accés à l'action :
```
@Override
    public boolean isEnabled() {
        return super.isEnabled() && getGuiContext().getUser().isAllowedTo(getSecurityFunction());
    }
```
- setSecurityFunction dont la modification de l'état du composant est exécutée dans un thread swing :
```
public void setSecurityFunction(String securityFunction) {
        this.securityFunction = securityFunction;
        GuiUtil.runInSwingThread(new Runnable() {
            public void run() {
                AbstractGuiAction.super.setEnabled(guiContext.getUser().isAllowedTo(getSecurityFunction()));
            }
        });
    }
```

Ces 2 modifications ne sont pas définitives dans la mesure où l'on doit observer la construction de mint sur sic pendant un certain temps (notamment en phase de livraison, phase à laquelle les TR impliqués avaient tendance à planter d'avantage).