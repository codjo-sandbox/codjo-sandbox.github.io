---
layout: post
title: agf-test - Ajout des steps concernant les emails dans le XSD
tags: [codjo-test,framework-1-36]
---
Ajout des balises suivantes dans le XSD :

```start-mail-server```
```send-mail```
```assert-inbox```

Exemple :
```
<start-mail-server port="25"/>

<send-mail from="maigret@allianz.fr" to="derrick@allianz.de" subject="Enquête" port="25">
    N'oublie pas les sandwiches.
</send-mail>

<assert-inbox>
    <message from="maigret@allianz.fr" to="derrick@allianz.de" subject="Enquête">
       <assertText value="sandwich"/>
    </message>
</assert-inbox>
```