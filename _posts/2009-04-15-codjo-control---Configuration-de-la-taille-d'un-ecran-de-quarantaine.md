---
layout: post
title: agf-control - Configuration de la taille d'un écran de quarantaine
tags: [framework-1-91,codjo-control,hot-topics]
---
La possibilité de configurer la taille d'un écran de quarantaine a été ajoutée.

Pour ce faire, il suffit de préciser les attributs ```windowWidth``` et/ou ```windowHeight``` de la balise correspondant à l'écran de quarantaine (dans le fichier **quarantine.xml**).

Cette configuration peut être réalisée sur un écran principal (balise ```window```) ou sur un écran de détail (balise ```detail```). Si les attributs ne sont pas précisés, les tailles par défaut sont assignées.

<u>Exemple de configuration sur un écran principal :</u>
```xml
<gui name="Emetteur" tooltip="Affiche la liste des emetteurs">
    <quarantine>Q_AP_ISSUER</quarantine>
    <window title="Quarantaine avec taille customisée" windowWidth="500" windowHeight="300">
        <preference>QUserIssuerWindow</preference>
        <filter>issuerCode</filter>
        <dbFilter>source</dbFilter>
        <dbFilter>user</dbFilter>
    </window>
</gui>
```