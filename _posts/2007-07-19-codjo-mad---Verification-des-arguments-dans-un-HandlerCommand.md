---
layout: post
title: agf-mad - Vérification des arguments dans un HandlerCommand
tags: [framework-1-6,codjo-mad]
---
Ajout d'une méthode qui vérifie que les arguments nécessaires au handler sont présent dans la requête.

```java
@Override
public CommandResult executeQuery(CommandQuery query) throws HandlerException {
    query.checkRequiredArguments("period", "family");
    ...
}
```