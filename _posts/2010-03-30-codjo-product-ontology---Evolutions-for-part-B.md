---
layout: post
title: agf-product-ontology - Evolutions for part B
tags: [framework-1-140,codjo-product-ontology]
---
<u>Context</u>:
Evolution of the existing webservice for part B.

<u>Description</u>:
- new fields for part B are added.
- new parameters have been added to ```GetProductAction```.

Now, the parameters for this call are:
- ```code```: the product code.
- ```date```: the selection date for the product.
- ```feesYear```: the year or the fees to use (only used for part B).
- ```partSelector```: useful to select the part A or B. 

 ```GetProductBisAction``` has been removed as it was only temporarily created for compatibility reasons.
