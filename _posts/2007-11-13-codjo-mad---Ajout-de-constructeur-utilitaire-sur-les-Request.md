---
layout: post
title: agf-mad - Ajout de constructeur utilitaire sur les Request
tags: [codjo-mad,framework-1-19]
---
Ajout de constructeur utilitaire sur les ```Request``` : ```CommandRequest```, ```DeleteRequest```, ```SelectRequest```, ```InserRequest```, ```UpdateRequest```, ```SqlRequest```.

<u>Exemple</u>
```java
SelectRequest select = 
  new SelectRequest("selectCurrency", new FieldsList("currencyCode", "EUR"));
```