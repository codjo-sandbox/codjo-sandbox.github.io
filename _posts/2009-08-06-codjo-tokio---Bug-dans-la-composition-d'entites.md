---
layout: post
title: agf-tokio - Bug dans la composition d'entités
tags: [framework-1-108,codjo-tokio]
---
La composition d'entité ne marchait pas dans le cas suivant :
```xml|title=tokio
<include-entities file="parent.entities"/>

<input>
  <create-entity name="parent">
    <parameter name="firstName" value="John"/>
  </create-entity/>

  <create-entity name="parent">
    <parameter name="firstName" value="Sarah"/>
  </create-entity/>
</input>
```

```xml|title=parent.entities
<include-entities file="child.entities"/>

<entity id="parent">
  <parameters>
    <parameter name="firstName"/>
  </parameters>

  <body>
    <create-entity name="child">
      <parameter name="firstName" value="@firstName@ Junior"/>
    </create-entity>
  </body>
</entity>
```

Les entités child étaient toutes les deux créées avec ```firstName="John Junior"```.

Cela a été corrigé.