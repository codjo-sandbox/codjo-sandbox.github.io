---
layout: post
title: agf-standalone-client - Ajout de la fonctionnalité d'autologin
tags: [codjo-standalone-client,framework-1-26]
---
Ajout de la fonctionnalité d'autologin pour le socle standalone-client.

```java
 public static void main(String[[]] args) throws Exception {

    StandaloneClient client = ...
    client.addPlugin(JdbcServerPlugin.class);
    ...
    client.show(args);        
}
```

Pour activer la fonction d'autologin, il suffit de passer les arguments dans l'ordre suivant :
   * login,
   * password,
   * dbUrl,
   * dbCatalog,
   * dbEncryptedDatabaseLogin,
   * dbEncryptedDatabasePassword

Par exemple pour les tests release, il suffit de configurer le fichier ```test-release.config``` comme suit :
{noformat}
gui.default.arg.0 = ${defaultTestUser}
gui.default.arg.1 = ${defaultTestUserPassword}
gui.default.arg.2 = ${jdbc.server}
gui.default.arg.3 = ${jdbc.catalog}
gui.default.arg.4 = ${encryptedDatabaseLogin}
gui.default.arg.5 = ${encryptedDatabasePassword}
{noformat}

