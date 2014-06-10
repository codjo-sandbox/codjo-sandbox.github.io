---
layout: post
title: agf-util - New methods in StringUtil
tags: [codjo-util,framework-1-143,codjo-segmentation,codjo-control,api-change]
---
<u>Context</u>:

Several methods in several libraries existed to convert java names to sql names (ex: "portfolioCode" to "PORTFOLIO_CODE") and reciprocally.


<u>Description</u>:

2 methods in ```StringUtil``` class have been added :

```public static String javaToSqlName(String javaName);

public static String sqlToJavaName(String sqlName);
```
Deprecated methods have been replaced by those above in the following libraries:

* codjo-segmentation
* codjo-control

<u>Examples</u>:

```StringUtil.javaToSqlName("securityId")
```returns ```"SECURITY_ID"```


```StringUtil.javaToSqlName("portfolioRate;holderCode")
```returns ```"PORTFOLIO_RATE;HOLDER_CODE"```


```StringUtil.sqlToJavaName("COMPANY_LABEL")
```returns "companyLabel"


See : [[codjo-util - Utilisation|agf-util - Utilisation]]