---
layout: post
title: agf-release-test - Contextual variables in assert tree step
tags: [framework-1-194,codjo-release-test]
---
<u>Context</u>
Variables like ```TODAY``` could not be used in assert tree steps. It was impossible to check a node in the tree if a date was present in the path.

<u>Description</u>
Variables are now properly expanded.

<u>Example</u>
```
<tstamp>
    <format property="TODAY" pattern="MM/dd/yyyy" locale="en"/>
</tstamp>

[[...]]

<assertTree name="tree" path="ROOT:Security 13:Creation date ${TODAY}" exists="true"/>
```

See [[assertTree|framework:codjo-release-test - Tags IHM#agf-release-test-TagsIHM-assertTree]]