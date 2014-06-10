---
layout: post
title: agf-test - Ajout d'un assertEquivalent sur XmlUtil
tags: [codjo-test,framework-1-8]
---
XmlUtil.assertEquivalent permet de comparer deux flux XML sans tenir compte de l'ordre.
&nbsp;
Exemple :
&nbsp;
```
XmlUtil.assertEquivalent("<a attribute='seb' id='toto'>"
                                + "  <field id='0' value='zero'/> "
                                + "  <field id='1' value='one'/> "
                                + "</a>",
                                   "<a attribute='seb' id='toto'>"
                                + "  <field id='1' value='one'/> "
                                + "  <field id='0' value='zero'/> "
                                + "</a>");
```