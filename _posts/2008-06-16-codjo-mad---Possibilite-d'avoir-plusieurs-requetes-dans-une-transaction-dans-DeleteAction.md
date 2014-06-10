---
layout: post
title: agf-mad - Possibilité d'avoir plusieurs requêtes dans une transaction dans DeleteAction
tags: [codjo-mad,framework-1-48]
---
Dans ```DeleteAction```, ajout d'une méthode ```getRequestsForRow()``` pouvant être surchargée.
Elle permet de renvoyer plusieurs ```Request``` qui seront exécutées dans une même transaction.

### Exemple :
```java
@Override
protected Request[[]] getRequestsForRow(Row row) {
    return new Request[[]]{buildDeleteWorkInProgress(row),
                         buildDeleteChanges(row),
                         buildDeleteProduct(row)};
}
```