---
layout: post
title: agf-test - New methods in XmlUtil
tags: [framework-1-134,codjo-test]
---
<u>Context</u>:
For [[framework:/2010/02/16/codjo-release-test - Asserting xml files]], it was needed to improve ```XmlUtil```.

<u>Description</u>:
```boolean XmlUtil.areEquals(String, String)``` and ```boolean XmlUtil.areEquivalent(String, String)``` have been implemented.

<u>Example</u>:
```java
if(XmlUtil.areEquals("<root>
                         <field>toto</field>
                         <field>tata</field>
                      </root>",
                     "<root>
                         <field>toto</field>
                         <field>tata</field>
                      </root>")) {
    System.out.println("Comparaison OK");
}

if(XmlUtil.areEquivalent("<root>
                              <field>toto</field>
                              <field>tata</field>
                          </root>",
                         "<root>
                              <field>tata</field>
                             <field>toto</field>
                          </root>")) {
    System.out.println("Comparaison OK");
}

```