---
layout: post
title: agf-mad - Internationalization of menus and actions
tags: [framework-1-184,codjo-mad]
---
<u>Context</u>
Applications need to be internationalized. Therefore, all framework libraries that expose GUI components or contain messages dedicated to the user have to be internationalized too.

<u>Description</u>
Menu entries and actions declared in the ```menu.xml``` file are automatically registered in i18n mechanism.

<u>Example</u>
```
<menubar>
    <menu>
        <name>com.agf.mint.gui.menu.Produit</name>
        <menu action="com.agf.mint.gui.product.ProductFrameAction"/>
    </menu>
...
</menubar>
```

<u>```i18n.properties```</u>
```
com.agf.mint.gui.menu.Produit=Produit
com.agf.mint.gui.product.ProductFrameAction=Affichage
com.agf.mint.gui.product.ProductFrameAction.tooltip=Liste des Produits - Caractéristiques
```

<u>```i18n_en.properties```</u>
```
com.agf.mint.gui.menu.Produit=Product
com.agf.mint.gui.product.ProductFrameAction=Show products
com.agf.mint.gui.product.ProductFrameAction.tooltip=Show products characteristics

```