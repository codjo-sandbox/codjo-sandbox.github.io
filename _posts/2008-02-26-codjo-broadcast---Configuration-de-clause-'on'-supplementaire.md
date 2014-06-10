---
layout: post
title: agf-broadcast - Configuration de clause 'on' supplémentaire
tags: [codjo-broadcast,framework-1-32]
---
Prise en compte de la modification de ```codjo-sql``` [[Configuration de clause 'on' supplémentaire|http://wp-confluence/confluence/pages/viewpage.action?pageId=3575735]].

<u>Exemple</u> : Configuration d'une jointure avec une clause ```on``` supplémentaire :
```java
public class CharacteristicsPreferences extends Preferences {
  ...
  @Override
  protected void initJoinKeys() {
    ...
    addJoinKeys(RIGHT_JOIN, "AP_INDIRECT_FEES as dsi", "AP_CLASS_CODIFICATION",
                new String[[][]]{
                      {"CLASS_CODIFICATION_CODE", "CLASS_CODIFICATION_CODE", " = "},
                      {"BEGIN_DATE", "BEGIN_DATE", "="}},
                JoinExpression.create().extraOnClause("and dsi.FEES_CODE='DSI'"));
    ...
```

