---
layout: post
title: agf-pom - New maven library available agf-maven-enforcer
tags: [framework-1-147,resolution-of-brin,hot-topics,codjo-pom,codjo-maven-enforcer]
---
<u>Context</u>:
{info:title=Resolution of BRIN}
Dependency version of some library modules were not set in libraries ```dependencyManagement```.
{info}

<u>Description</u>:
To detect such missing dependencies, a custom detection rule has been created in ```codjo-maven-enforcer```.
This custom rule is used by ```maven-enforcer-plugin``` and is played against the libraries.
see: [[framework:codjo-maven-enforcer]]