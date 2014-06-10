---
layout: post
title: agf-maven-common - Enhancement of ArtifactDescriptor code
tags: [framework-1-124,codjo-maven-common]
---
<u>Context</u>:
Duplicated code has been found inside plugins (```Include``` class in plugins which duplicates the code from ```ArtifactDescriptor```).

<u>Description</u>:
```ArtifactDescriptor``` has been enhanced:
* ```void resolveIncludeVersion(DependencyManagement dependencyManagement)```: does nothing in case a version is already set, otherwise search into ```dependencyManagement``` for version,
* ```void resolveType(String type)```: does nothing in case a type is already set, otherwise set the type.