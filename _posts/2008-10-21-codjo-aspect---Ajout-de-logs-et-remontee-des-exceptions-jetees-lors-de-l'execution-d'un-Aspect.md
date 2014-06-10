---
layout: post
title: agf-aspect - Ajout de logs et remontée des exceptions jetées lors de l'éxécution d'un Aspect
tags: [framework-1-67,codjo-aspect]
---
Certaines exceptions levées lors de l'exécution d'un Aspect étaient écrasées par d'autres exceptions, gérées elles dans ces mêmes aspects.

En effet un certain nombre d'exceptions (_TransactionException, AspectException, PointRunnerException_), sont traitées lors de l'exécution de la méthode _run()_ de la classe _TransactionalPoint_ qui lance les Aspects.

Mais la gestion de ces exceptions était telle qu'elle écrasait toutes les autres exceptions qui pouvaient survenir lors de l'exécution de cet Aspect, comme par exemple une _NullPointerException_, ce qui menait&nbsp; à des problèmes pour déboguer.

L'ajout dans la méthode _run()_ de _TransactionalPoint_ d'un _catch_ supplémentaire :
```
catch (Throwable e) {
    txManager.rollback(context);
    throw new PointRunnerException(e.getLocalizedMessage(), e);
}
```

permet donc de logger plus généralement toutes les autres exceptions.
\\
\\
\\