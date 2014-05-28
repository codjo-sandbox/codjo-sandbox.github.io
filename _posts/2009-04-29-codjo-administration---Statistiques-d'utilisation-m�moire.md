---
layout: posttitle: agf-administration - Statistiques d'utilisation m�moire
tags: [framework-1-93,codjo-administration]
---
La lib ```codjo-administration``` permet de sauvegarder p�riodiquement dans un fichier les statistiques d'utilisation m�moire.
Par d�faut, un relev� est fait toutes les 5 min. Ce relev� comprend la m�moire utilis�e ainsi que la m�moire totale.

Cet audit est d�sactiv� par d�faut. L'activation peut-�tre faite des deux mani�res suivantes :
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
