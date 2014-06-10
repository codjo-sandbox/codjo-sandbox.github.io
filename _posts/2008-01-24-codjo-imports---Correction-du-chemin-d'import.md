---
layout: post
title: agf-imports - Correction du chemin d'import
tags: [codjo-imports,framework-1-28]
---
Dans un test release d'import, afin de pouvoir tester le chemin du fichier à importer situé dans le champ ```ARGUMENT``` de la table ```AP_WORKFLOW_LOG```, un caractère '/' ou '\' est ajouté à la fin du répertoire du fichier d'import.

Dans les applications utilisant ```codjo-imports``` et dans les tests release utilisant la balise ```<copy-to-inbox ... />```,  ce chemin est testable de la façon suivante:

Dans le fichier ```.tokio```:
```xml
...
<table name="AP_WORKFLOW_LOG" ...>
...
<field name="REQUEST_TYPE" value="import"/>
<field name="ARGUMENT" value="import.source.folder=${java.io.tmpdir}&#10;import.fileName=FICHIER_A_IMPORTER.txt"/>
...
</table>
...
```