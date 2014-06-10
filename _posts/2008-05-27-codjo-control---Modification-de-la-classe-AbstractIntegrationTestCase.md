---
layout: post
title: agf-control - Modification de la classe AbstractIntegrationTestCase
tags: [codjo-control,framework-1-46,hot-topics]
---
Jusqu'ici chaque TU de plan d'intégration SQL dérivant de la classe **AbstractIntegrationTestCase** chargeait la liste des plans de l'application pour chaque test. Par souci d'optimisation, des modifications ont été effectuées :
- A présent, l'appel se fait de la manière suivante :
```
public ImportDividendControlTest() {
    super("Dividend.xml");
}
```
où le fichier xml représente le plan d'intégration de l'entité

- Les plans d'intégration et les TU doivent être dans le même package. Exemple
```xml
+ appli-server
     + src
        + main
           + resources
               + com/agf/appli/server/control/dividend/Dividend.xml
        + test
           + java
               + com/agf/appli/server/control/dividend/DividendIntegrationTest.java
```

- Le fichier **ApplicationIP.xml** doit tenir compte du nouveau chemin :
```
<application-controls name="MINT">
    <integration-definition>
        <plan>/com/agf/mint/server/control/dividend/Dividend.xml</plan>
    </integration-definition>
    ...
</application-controls>
```

Cette modification n'étant pas rétro-compatible les projets RED, MINT, ICOMP et GABI qui l'utilisent ont été migrés sur la nouvelle version de la lib.