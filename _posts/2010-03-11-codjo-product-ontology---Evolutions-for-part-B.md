---
layout: post
title: agf-product-ontology - Evolutions for part B
tags: [codjo-product-ontology,framework-1-139]
---
<u>Context</u>:
Evolution of the existing webservice for part B.

<u>Description</u>:
- new fields for part B are added
- a new signature is created to call the service for part A or B. The old one is kept for compatibility, but will be removed when the development is over.

```java
 GetProductBisAction extractGetProductBisAction(AclMessage request)
```

The parameters for this new call are:
- ```code```: the product code
- ```date```: the selection date for the product
- ```partSelector``` : useful to select the part A or B. 
- ```feesYear```: the year or the fees to use (only used for part B)
