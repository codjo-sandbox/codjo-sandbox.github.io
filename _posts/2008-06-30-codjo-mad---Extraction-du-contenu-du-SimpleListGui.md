---
layout: post
title: agf-mad - Extraction du contenu du SimpleListGui
tags: [codjo-mad,framework-1-50]
---
Nous avons extrait le panel de l'internal frame ```SimpleListGui``` dans une nouvelle classe ```SimpleListPanel``` de façon à la rendre réutilisable.

{note:title=Be Careful}
Il y a un problème de conception sur ```SimpleListGui``` car certains attributs sont déclarés protected et sont utilisés directement dans certains projets alors qu'il y a des accesseurs prévus à cette effet. (cela empêche de refactorer proprement la classe)

Exemple dans mint ```PerfHistoListGui``` l'accès à la ```RequestTable``` devrait se faire par l'accesseur.
```
public class PerfHistoListGui extends SimpleListGui{

public void init(GuiContext guiContext, String preference) {
         table.setPreference(preference);
     }
[[..]]
```

Il faudrait que chacun corrige cela en passant par le getter plutôt que par l'attribut afin de pouvoir repasser en private les attributs de ```SimpleListGui``` de la librairie codjo-mad.

A cette fin, les attributs ont été passés ```Deprecated```
```
    /****
     * @deprecated Utiliser #getTable plutôt que d'utiliser directement l'attribut dans les sous-classes
     * @TODO : à passer en private lorsque cet attribut ne sera plus utilisé par les sous-classes
     */
    @Deprecated
    protected RequestTable table = new RequestTable();
    /****
     * @deprecated Utiliser #getToolBar plutôt que d'utiliser directement l'attribut dans les sous-classes
     * @TODO : à passer en private lorsque cet attribut ne sera plus utilisé par les sous-classes
     */
    @Deprecated
    protected RequestToolBar toolBar = new RequestToolBar();
```
{note}