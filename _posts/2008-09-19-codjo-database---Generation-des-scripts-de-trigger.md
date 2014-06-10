---
layout: post
title: agf-database - Génération des scripts de trigger
tags: [framework-1-62,codjo-database]
---
La classe ```DatabaseScriptHelper``` permet maintenant de créer des scripts de trigger (_drop_, _create_ et _log_) sous Sybase.
Ces méthodes sont utilisées principalement dans ```datagen```.

<u>Exemple</u> : drop de TR_AP_TOTO_I"
```java
import static com.agf.database.common.util.SqlTrigger.triggerNamed;

...

databaseScriptHelper.buildDropTriggerScript(triggerNamed("TR_AP_TOTO_I"));
```

<u>Exemple</u> : create de TR_AP_TOTO_I"
```java
import static com.agf.database.common.util.SqlTrigger.insertTrigger;
import static com.agf.database.common.util.SqlTable.tableNamed;

...

databaseScriptHelper.buildCreateTriggerScript(insertTrigger("TR_AP_TOTO_I",
                                                            tableNamed("AP_TOTO"),
                                                            "// CUSTOM SQL CODE")));
```

<u>Exemple</u> : log de TR_AP_TOTO_I"
```java
import static com.agf.database.common.util.SqlTrigger.triggerNamed;

...

databaseScriptHelper.buildLogTriggerCreationScript(triggerNamed("TR_AP_TOTO_I"));
```