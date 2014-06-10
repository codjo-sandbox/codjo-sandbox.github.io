---
layout: post
title: agf-release-test - Modification comportement balise vtom pour le mode local
tags: [framework-1-52,codjo-release-test]
---
Dans la balise <vtom>  pour le mode local, le paramètre ```configuration``` est automatiquement ajouté si la propriété "batch.configuration" est définie, ainsi qu'au moins une ligne <arg line="..."/>.

exemple MyTR.xml
```
...
<vtom user="user_tr" batchType="prodcom">
  <arg line="-date &quot;2008-07-09&quot;"/>
</vtom>
...
```
test-release.config
```
...
batch.configuration  = ${project.basedir}/target/config/batch-local.config
...
```

équivalent à MyOldTR.xml
```
...
<vtom user="user_tr" batchType="prodcom">
  <arg line="-configuration &quot;${project.basedir}/target/config/batch-local.config&quot;"/>
  <arg line="-date &quot;2008-07-09&quot;"/>
</vtom>
...
```