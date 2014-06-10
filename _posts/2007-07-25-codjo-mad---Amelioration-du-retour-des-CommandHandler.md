---
layout: post
title: agf-mad - Amelioration du retour des CommandHandler
tags: [framework-1-7,codjo-mad]
---
Amélioration de la capacité de retour des ```HandlerCommand```. Il est maintenant possible de préciser le nom du champ résultat de la commande.

<u>Par exemple :</u>

```java
public class MyStuffCommand extends HandlerCommand {

    @Override
    public CommandResult executeQuery(CommandQuery query) {
        return createResult("myValue", computeAssetSleeveId());
    }
    ....
}
```

Ensuite côté IHM, il suffit de faire 

```java
MadConnectionPlugin mad = ...;
Result result = mad.getOperations().sendRequest(new CommandRequest("myStuff"));
String myValue = result.getValue(0, "myValue");
```
