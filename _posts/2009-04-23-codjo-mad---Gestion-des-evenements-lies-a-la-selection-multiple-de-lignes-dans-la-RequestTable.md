---
layout: post
title: agf-mad - Gestion des évènements liés à la sélection multiple de lignes dans la RequestTable
tags: [framework-1-93,codjo-mad,hot-topics]
---
<u>Contexte</u>
Mint doit gérer l'état d'un bouton en fonction des lignes sélectionnées d'une table.

<u>Problème</u>
Dans la classe ```RequestTable```, l'envoi de l'évènement "**selectedRow**" (lié à la sélection de lignes) était mal géré. Seule la première ligne sélectionnée était sauvegardée dans la ```DataSource``` puis l'évènement envoyé contenait l'ancienne ligne sélectionnée et la nouvelle.
Dans le cas d'une sélection multiple incrémentale (CTRL-Bouton Souris Gauche), l'évènement "**selectedRow**" n'était pas envoyé lorsque l'ancienne première ligne sélectionnée était identique à la nouvelle première ligne sélectionnée (comportement normal du PropertySupport).

<u>Solution</u>
L'évènement "**selectedRow**" est envoyé systématiquement et contient un objet ```SelectionDataSource``` (créé pour gérer l'ensemble des lignes sélectionnées d'une ```RequestTable```) et non plus un objet ```Row```.

<u>Usage</u>
Sur la classe ```SelectionDataSource```, un ensemble de méthodes est proposé :
* _getRow()_ : renvoie la première ligne sélectionnée,
* _getRows()_ : renvoie la liste des lignes sélectionnées,
* _isEmpty()_ : vrai si la la liste des lignes sélectionnées est vide, faux sinon.

<u>Exemple</u>
```
private class MyPropertyChangeListener implements PropertyChangeListener {

    public void propertyChange(PropertyChangeEvent event) {

        for (Row selectedRow : ((SelectionDataSource)event.getNewValue()).getRows()) {
            ...
        }

        ...
    }
}
```