---
layout: post
title: agf-aspect - Attribut argument optionnel
tags: [framework-1-96,codjo-aspect]
---
Dans la configuration d'un ```aspect```, l'attribut ```argument``` de la balise ```join-point``` est maintenant optionnel.

<u>Exemple</u>
```xml
<aspect id="MyAspect" class="com.agf.sam.MyAspect">
    <join-points>
        <join-point call="before" point="sendAudit" />
    </join-points>
</aspect>
```
