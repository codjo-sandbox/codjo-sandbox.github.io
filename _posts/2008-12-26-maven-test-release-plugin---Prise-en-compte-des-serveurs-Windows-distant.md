---
layout: post
title: maven-test-release-plugin - Prise en compte des serveurs Windows distant
tags: [framework-1-77,maven-test-release-plugin,hot-topics]
---
Il est maintenant possible de configurer un serveur d'intégration distant de type Windows (implémenté sous forme de service Windows).

<u>Exemple</u> DELRECO : La machine d'intégration est ```bi-delreco``` le nom du service sur cette machine est ```DELRECO_INT```. Dans ce cas il suffit dans le ```pom``` applicatif de configurer le profil ```server-integration``` comme suit :
```xml
...
<profile>
    <id>server-integration</id>
    <activation>
        <property>
            <name>server</name>
            <value>integration</value>
        </property>
    </activation>
    <properties>
        <remote>true</remote>
        <serverHost>bi-delreco</serverHost>
        <windowsApplicationDirectory>\\bi-delreco\delreco$\APP</windowsApplicationDirectory>
        <windowsServiceName>DELRECO_INT</windowsServiceName>
    </properties>
</profile>
...
```
