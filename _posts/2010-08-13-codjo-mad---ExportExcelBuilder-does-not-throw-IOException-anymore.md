---
layout: post
title: agf-mad - ExportExcelBuilder does not throw IOException anymore
tags: [framework-1-160,api-change,codjo-mad]
---
<u>Context</u>
2 methods (```generate``` and ```buildExcelDatas```) of ```ExportExcelBuilder``` class were defined as if they threw ```IOException```. But, in fact, it was impossible that they do throw such exception.

<u>Description</u>
The signature of the methods has been changed to show that they do not throw any ```IOException```.