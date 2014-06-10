---
layout: post
title: agf-database - Ergonomie de code du JdbcFixture
tags: [framework-1-63,codjo-database]
---
La classe ```JdbcFixture``` a été modifiée afin de prendre en compte quelques règles d'ergonomie de code.
De nombreuses méthodes ont été mises _@deprecated_ afin d'être remplacées.
Le nommage des méthodes ainsi que leur signature ont été unifiés.
De plus, les fonctionnalités du ```fixture``` ont été divisées en trois groupes d'utilisation (normale, avancée et utilitaire).

<u>Exemple</u> : utilisation normale
```java
JdbcFixture jdbcFixture = JdbcFixture.newFixture();
jdbcFixture.create("AP_TOTO", "LABEL varchar(200) not null, CODE int");

...

jdbcFixture.assertTableIsEmpty("AP_TOTO");
```

<u>Exemple</u> : utilisation avancée
```java
import static com.agf.database.common.util.SqlIndex.index;
import static com.agf.database.common.util.SqlTable.table;

...

jdbcFixture.advanced().assertExists("AP_TOTO");
jdbcFixture.advanced().assertExists(table("AP_TOTO"));
jdbcFixture.advanced().assertExists(index("X1_AP_TOTO", table("AP_TOTO")));
```


<u>Exemple</u> :
```java
import static com.agf.database.common.util.SqlTable.table;

...

jdbcFixture.util().spoolQueryResult("select * from AP_TOTO", System.out);
jdbcFixture.util().spool(table("AP_TOTO"));
```