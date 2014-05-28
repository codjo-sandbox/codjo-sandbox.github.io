---
layout: posttitle: agf-administration - Activation des logs sur les handlers
tags: [framework-1-93,codjo-administration,hot-topics]
---
Le plugin ```AdministrationServerPlugin``` offre la possibilit� de configurer l'audit des ```handlers```.

Cette configuration est rendue possible des deux mani�res suivantes :
* server-config.properties :
```xml
AdministrationService.recordHandlerStatistics = true
AdministrationService.recordDestinationFile   = c:\dev\user\temp\sample.log
```

* AdministrationServerConfiguration :
```java
public MyApplicationServerPlugin(AdministrationServerPlugin administration) {
    administration.getConfiguration().setRecordHandlerStatistics(true);
    administration.getConfiguration().setRecordDestinationFile("c:\\dev\user\\temp\\sample.log");
}
```

