---
layout: post
title: agf-mad - Mécanisme d'écoute des listeners
tags: [framework-1-94,codjo-mad]
---
Il est maintenant possible d'enregistrer des listener qui seront alertés avant et après l'exécution d'```handlers```.

<u>Exemple</u> : d'utilisation de la méthode ```getOperations()``` de ```MadServerPlugin``` pour enregistrer/désenregistrer un listener :
```java
MadServerPlugin madServerPlugin = ...;
HandlerListener handlerListener = new HandlerListener() {
    public void handlerStarted(Handler handler, HandlerContext handlerContext) {
        ...
    }

    public void handlerStopped(Handler handler, HandlerContext handlerContext) {
        ...
    }
}
madServerPlugin.getOperations().addHandlerListener(handlerListener);
...
madServerPlugin.getOperations().removeHandlerListener(handlerListener);
```