---
layout: post
title: agf-mad - Modification de ButtonPanelLogic
tags: [framework-1-60,codjo-mad]
---
Suite à la dernière modification de la classe **ButtonPanelLogic**, un composant de MINT qui en dérivait **MintButtonPanelLogic** ne fonctionnait plus dans le cas où la fenêtre ne se fermait pas après enregistrement des données. En effet dans **MintButtonPanelLogic**, la mécanique du chargement de données de la datasource est différente de celle de **ButtonPanelLogic** (prise en charge des DetailDataSource et ListDataSource).

Afin de garder la mécanique actuelle dans ButtonPanelLogic, une méthode protégée **doReload()** qui englobe le **datasource.load()** a été créee. Ainsi dans MintButtonPanelLogic, on peut surcharger cette méthode et appliquer un load spécifique.\\

```title=ButtonPanelLogic.java
protected void executeOk() {
        boolean doArchive = false;
        try {
            if (isArchivable() && isUserRequestToArchive()) {
                doArchive = true;
                doArchive();
            }
            else {
                if (isMustSave()) {
                    doSave();
                }
            }
            if (!errorCheckerList.hasError()) {
                if (!isCloseOnSave()) {
                    doReload();
                }
                closeDetailWindow(SAVE_ACTION);
            }
            else {
                errorCheckerList.clearError();
            }
        }
        catch (RequestException ex) {
            handleError(doArchive, ex);
        }
        catch (RuntimeException ex) {
            handleError(doArchive, ex);
        }
    }


    protected void doReload() throws RequestException {
        mainDataSource.load();
    }
```

Dans Mint :
```title=MintButtonPanelLogic.java
...
@Override
    protected void doReload() throws RequestException {
        if (listDataSource != null) {
            listDataSource.load();
        }
        else {
            getMainDataSource().load();
        }

        for (Object obj : getSubDataSourceList()) {
            DataSource dataSource = (DataSource)obj;
            if (dataSource.hasBeenUpdated()) {
                dataSource.load();
            }
        }
    }
...
```