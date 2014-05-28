---
layout: posttitle: agf-administration - Configuration du r�pertoire de log
tags: [framework-1-96,codjo-administration]
---
Le r�pertoire de log peut �tre sp�cifi� de diff�rentes mani�res.
La priorisation de cette configuration a �t� revue.
Les voici, par priorit� d�croissante :
* Via le server-config.properties en ajoutant la propri�t� suivante :
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
