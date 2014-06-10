---
layout: post
title: agf-mad - Modification du DetailDataSource
tags: [codjo-mad,framework-1-33]
---
La taille max des ```JTextComponent``` et des ```NumberField``` liés à des ```DetailDataSource``` peut être renseignée automatiquement.
Pour la mise en place de cette mécanique, il faut fournir au ```DetailDataSource``` le nom de l'entité référente.

Exemple :
```java
DetailDataSource detailDataSource = ...;
detailDataSource.setEntityName("anEntityName");
```