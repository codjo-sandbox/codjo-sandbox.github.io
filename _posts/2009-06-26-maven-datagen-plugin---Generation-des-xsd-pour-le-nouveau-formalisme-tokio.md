---
layout: post
title: maven-datagen-plugin - Génération des xsd pour le nouveau formalisme tokio
tags: [kaizen-tr,framework-1-102,maven-datagen-plugin,hot-topics]
---
{info:title=Dans le cadre du Kaizen TR}{info}

Un nouveau goal ```generate-tokio-xsds``` a été créé.
Il permet de générer les fichiers ```xsd``` utilisés dans le nouveau formalisme tokio.

Ce goal est automatiquement appelé lors de l'exécution d'idea.cmd et crée les fichiers dans ```c:\dev\platform\cache\xsd```.

Les fichiers tokio et entities doivent y faire référence afin de bénéficier de leurs avantages.

<u>Exemple d'utilisation</u>
```xml
<entities xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xsi:noNamespaceSchemaLocation="file:C:/dev/platform/cache/xsd/mint-entities.xsd">
...
</entities>

<story xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:noNamespaceSchemaLocation="file:C:/dev/platform/cache/xsd/mint-story.xsd">
...
</story>

<cases xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:noNamespaceSchemaLocation="file:C:/dev/platform/cache/xsd/mint-cases.xsd">
...
</cases>

<Scenarii name="AUTOMATIC"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xsi:noNamespaceSchemaLocation="file:C:/dev/platform/cache/xsd/mint-scenarii.xsd">
...
</Scenarii>
```