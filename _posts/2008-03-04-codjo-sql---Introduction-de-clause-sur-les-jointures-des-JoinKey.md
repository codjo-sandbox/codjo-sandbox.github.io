---
layout: post
title: agf-sql - Introduction de clause sur les jointures des JoinKey
tags: [codjo-sql,framework-1-33]
---
Introduction de la notion de extraOnClause sur la JoinKeyExpression.
Exemple pour rajouter une clause sur une inner join :

```java
 addJoinKeys(INNER_JOIN, "AP_INDIRECT_FEES as dei", "AP_CLASS_CODIFICATION",
   new String[[][]]{
   {"CLASS_CODIFICATION_CODE", "CLASS_CODIFICATION_CODE", " = "},
   JoinExpression.create().extraOnClause("and dei.FEES_CODE='DEI'"));
```