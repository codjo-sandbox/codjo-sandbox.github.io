---
layout: posttitle: agf-administration - Configuration du répertoire de log
tags: [framework-1-96,codjo-administration]
---
Le répertoire de log peut être spécifié de différentes manières.
La priorisation de cette configuration a été revue.
Les voici, par priorité décroissante :
* Via le server-config.properties en ajoutant la propriété suivante :
```
    AdministrationService.auditDestinationDir = ${log.dir}
```
* Via la configuration AdministrationServerConfiguration :
```java
public MyApplicationServerPlugin(AdministrationServerPlugin administration) {
    administration.getConfiguration().setAuditDestinationDir("c:\\dev\\user\\temp");
}
```
* Via l'argument JVM ```-Dlog.dir=...```
