---
layout: posttitle: agf-administration - Internationalization bootstrap
tags: [framework-1-184,codjo-administration]
---
<u>Context</u>
Applications need to be internationalized. Therefore, all framework libraries that expose GUI components or contain messages dedicated to the user have to be internationalized too.

<u>Description</u>
The action that allows to launch the server administration window has been internationalized. The following keys have been added in the i18n properties files:

<u>```i18n.properties```</u>
```
com.agf.administration.gui.plugin.AdministrationGuiPlugin#AdministrationAction=Administration du serveur
com.agf.administration.gui.plugin.AdministrationGuiPlugin#AdministrationAction.tooltip=Administration du serveur

```

<u>```i18n_en.properties```</u>
```
com.agf.administration.gui.plugin.AdministrationGuiPlugin#AdministrationAction=Server administration
com.agf.administration.gui.plugin.AdministrationGuiPlugin#AdministrationAction.tooltip=Server administration

```