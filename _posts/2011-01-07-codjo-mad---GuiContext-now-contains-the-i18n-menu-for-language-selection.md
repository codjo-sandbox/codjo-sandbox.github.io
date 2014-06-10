---
layout: post
title: agf-mad - GuiContext now contains the i18n menu for language selection
tags: [framework-1-182,codjo-mad]
---
<u>Context</u>
```codjo-i18n``` library defines a ```JMenu``` that allows users to select the language they want the application to work with.

<u>Description</u>
This menu is added by ```codjo-mad``` in ```GuiContext``` to facilitate the integration in applications. The property name is "Menu Langues". It allows applications that want to be internationalizable and that depend upon ```agf-mad``` to declare this property in their ```menu.xml``` configuration file as follows:

```
...
    <menu>
        <name>Administration</name>
        <menu plugin="com.agf.security.gui.plugin.SecurityGuiPlugin" actionId="UserForm"/>
        <menu separator="true"/>
        <menu action="com.agf.mint.gui.benchmark.control.BenchMarkControlAction"/>
        <menu separator="true"/>
        <menu action="com.agf.mint.gui.productfamily.ProductFamilyAction"/>
    </menu>
    <menu gui_contexte_property="Menu Langues"/>
    <menu gui_contexte_property="Menu Fenetre"/>
    <menu>
        <name>Aide</name>
        <menu action="com.agf.mad.gui.base.AboutWindowAction"/>
    </menu>
...
```