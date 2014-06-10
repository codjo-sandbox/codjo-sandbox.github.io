---
layout: post
title: agf-imports - New functions available for filtering expressions
tags: [framework-1-126,codjo-imports,hot-topics]
---
<u>Context</u>
When importing files via codjo-imports library:
* it is possible to reject some lines according to some expressions.
* it is possible to alter the value of the field to be imported according to a given expression.

Until now, "util.extractField" was the only utility function available. It allowed to parse the line according to a given separator to extract a specific value.

<u>Description</u>
Some new utility functions are now available. See below for API.

```
BigDecimal round(BigDecimal value, int precision);
Date extractDateFrom(String line, String format, String delimiter, String locale);
String removeChar(String value, String aChar);
Date stringToDate(String value, String format, String locale);
BigDecimal stringToDecimal(String value, String format);
```

<u>Example</u>
```
* utils.round(Valeur, 100)
-> prints 5,67 if "Valeur" equals to 5.665789 and 5,66 if "Valeur" equals to 5.664123.

* utils.extractDateFrom(Valeur, "dd/MM/yyyy", " ", "FRENCH")
-> prints corresponding object of Date type if "Valeur" equals "je veux récupérer 22/09/2006 sous forme de Date."

* utils.removeChar(Valeur, "\"")
-> removes all quotes in "Valeur"

* utils.stringToDate(Valeur, "dd/MM/yyyy", "FRENCH")
-> converts String "Valeur" into corresponding objet of Date type.

* utils.stringToDecimal(Valeur, "#.######")
-> convertit la String Valeur en objet de type BigDecimal selon le format correspondant.
```