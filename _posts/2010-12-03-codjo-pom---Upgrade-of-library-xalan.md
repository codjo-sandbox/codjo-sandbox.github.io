---
layout: post
title: agf-pom - Upgrade of library xalan
tags: [framework-1-177,codjo-pom,codjo-datagen,maven-datagen-plugin,codjo-mad,hot-topics]
---
<u>Context</u>:
```sif``` has problems with datagen generation failing in ```OutOfMemoryException```.
Next version of ```xalan``` should solve it.

<u>Description</u>:
* ```xalan``` has been upgraded to 2.7.1
* ```xalan:serializer:2.7.1``` has been added
* ```xml-apis``` has been upgraded to 1.3.04

Some minor modifications have been made in ```datagen``` and ```mad```.

{note:title=New issues}
* By default, xsl transformation won't throw exceptions any more. Instead, it will be logged.
```datagen``` has been modified to ensure ascendant compatibility.
\\
To change this behaviour, you have to do:
```
Transformer transformer;
...
transformer.setErrorListener(new DefaultErrorHandler(true));
```
* ```Locale``` is taken into account in exception messages.
* Encoding specified in xsl is now taken into account.
{note}
