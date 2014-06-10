---
layout: post
title: agf-mad - Ajout xsd pour toolbar.xml
tags: [codjo-mad,framework-1-27]
---
Un fichier **toolbar.xsd** a été ajouté dans la librairie _codjo-mad_, afin de pouvoir valider le contenu et permettre l'auto-complétion des balises du fichier toolbar.xml (configuration de la toolbar principale).

Mise en place:
* Dans le fichier toolbar.xml, ajouter dans la balise racine les attributs suivants
**** xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
**** xsi:noNamespaceSchemaLocation="toolbar.xsd"

Exemple:
```xml
<toolbar xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="toolbar.xsd">
    <component action="com.agf.mad.gui.base.QuitAction"/>
</toolbar>
```
\\
* Dans IntelliJ, ajouter la référence ```Z:/maven/repository/codjo-mad/xsds/toolbar.xsd``` dans les préférences (cliquer sur File->Settings->Resources).