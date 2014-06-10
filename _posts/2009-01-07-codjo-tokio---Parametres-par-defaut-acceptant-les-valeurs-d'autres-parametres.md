---
layout: post
title: agf-tokio - Paramètres par défaut acceptant les valeurs d'autres paramètres
tags: [codjo-tokio,framework-1-78]
---
Lors de la définition d'une entité, il est maintenant possible d'avoir des paramètres par défaut qui prennent en compte les valeurs d'autres paramètres. A l'utilisation, cela permet de limiter le nombre de paramètres de certaines entités.

```xml|title=Exemple de définition d'entité
<entities>
    <entity id="Underlying">
        <parameters>
...
            <parameter name="LibGenericFund" default="Phoenix"/>
            <parameter name="LibClassFund" default="@LibGenericFund@ - Class"/>
...
        </parameters>
        
        <body>
           ...
        </body>
    </entity>
</entities>
```

A l'utilisation, si on spécifie uniquement le paramètre "LibGenericFund" à "W Finance", alors le paramètre "LibClassFund" aura par défaut la valeur "W Finance - Class".