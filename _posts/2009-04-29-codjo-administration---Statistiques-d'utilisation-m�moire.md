---
layout: posttitle: agf-administration - Statistiques d'utilisation mémoire
tags: [framework-1-93,codjo-administration]
---
La lib ```codjo-administration``` permet de sauvegarder périodiquement dans un fichier les statistiques d'utilisation mémoire.
Par défaut, un relevé est fait toutes les 5 min. Ce relevé comprend la mémoire utilisée ainsi que la mémoire totale.

Cet audit est désactivé par défaut. L'activation peut-être faite des deux manières suivantes :
* server-config.properties :
```xml
AdministrationService.recordMemoryUsage = true
AdministrationService.recordDestinationFile = c:\dev\user\temp\sample.log
```

* AdministrationServerConfiguration :
```java
public MyApplicationServerPlugin(AdministrationServerPlugin administration) {
    administration.getConfiguration().recordMemoryUsage(true);
    administration.getConfiguration().setRecordDestinationFile("c:\\dev\user\\temp\\sample.log");
}
```
