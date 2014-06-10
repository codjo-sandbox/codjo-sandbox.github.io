---
layout: post
title: agf-mad - Lien entre DataSource et entité
tags: [codjo-mad,framework-1-46]
---
Il est maintenant possible de préciser le nom de l'entité associée à un écran-liste dans les préférences via la balise ```entity```.

Exemple :
```
<preference id="DirectFeesScaleList">
  <entity>DirectFeesScale</entity>
  <selectAll>selectDirectFeesScaleForClassifier</selectAll>
  <insert>newDirectFeesScale</insert>
  <delete>deleteDirectFeesScale</delete>
  <update>updateDirectFeesScale</update>
  <column fieldName="priority" label="#" preferredSize="2"/>
  <column fieldName="scalePartLabel" label="Dénomination" preferredSize="180"/>
</preference>
```

De plus, le stockage du nom de l'entité a été remonté dans ```AbstractDataSource```.