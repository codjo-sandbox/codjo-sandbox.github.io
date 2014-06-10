---
layout: post
title: agf-imports - API change for utility function "round" in expressions
tags: [codjo-imports,hot-topics,framework-1-130]
---
<u>Context</u>
When importing files via codjo-imports library:
* it is possible to reject some lines according to some expressions.
* it is possible to alter the value of the field to be imported according to a given expression.

Until now, the "round" utility function was used as follows:
```
utils.round(Valeur, 100)
-> prints 5,67 if "Valeur" equals to 5.665789 and 5,66 if "Valeur" equals to 5.664123.
```

The way the precision had to be defined was not very user-friendly.

<u>Description</u>
Now, the precision is defined by the number of digits to take into account for the round function as follows:
```
utils.round(Valeur, 2)
-> prints 5,67 if "Valeur" equals to 5.665789 and 5,66 if "Valeur" equals to 5.664123.
```

