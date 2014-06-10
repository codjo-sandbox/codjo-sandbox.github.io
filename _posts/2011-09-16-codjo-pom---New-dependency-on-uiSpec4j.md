---
layout: post
title: agf-pom - New dependency on uiSpec4j
tags: [framework-1-211,codjo-pom,hot-topics]
---
<u>Context :</u>
To allow projects and framework to migrate on jdk16, we need to upgrade ```uispec4j``` from ```1.4-toolkit``` to ```2.4```.

<u>Description :</u>
The new ```uispec4j``` version (2.4) has changed its ```groupId```. As a consequence, a new dependency has been added in ```codjo-pom```.
As this version is provided for jdk5 and jdk6, we added two new profiles to deal with the dependency classifier.

{warning:title=Warning Incompatibility with jfcunit}
With 1.4-toolkit, we needeed to customize some class to avoid incombatibility problems between ```jfcunit``` and ```uispec4j```.
These modifications have not been yet reported in 2.4 version.
{warning} 

<u>Example</u>: 
In your application, you need to add the classifier:

```
  <dependency>
      <groupId>org.uispec4j</groupId>
      <artifactId>uispec4j</artifactId>
      <classifier>${envClassifier}</classifier>
      <scope>test</scope>
  </dependency>
```

The classifier ```envClassifier``` is automatically filled using an codjo-pom profile.
