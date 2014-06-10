---
layout: post
title: agf-release-test - Asserting xml files
tags: [framework-1-134,codjo-release-test,hot-topics]
---
<u>Context</u>:
For ```damas``` software, it was needed to assert file with xml content during release test. 

<u>Description</u>:
* By now, ```file-assert``` can check the equivalence of files containing xml.
* It is also possible to specify the comparison type using ```comparisonType``` attribute. It can be set to xls, pdf or xml.
By default, file extension will determine the comparison type.

see: [[framework:file-assert]]

<u>Example</u>:
```xml
 <file-assert expected="etalon.xml" actual="actual.xml"/>
```

```xml
 <file-assert expected="etalon.model" actual="actual.model" comparisonType="xml"/>
```