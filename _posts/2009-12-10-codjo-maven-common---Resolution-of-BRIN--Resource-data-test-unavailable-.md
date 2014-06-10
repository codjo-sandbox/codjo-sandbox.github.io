---
layout: post
title: agf-maven-common - Resolution of BRIN "Resource data-test unavailable"
tags: [hot-topics,framework-1-126,codjo-maven-common,resolution-of-brin]
---
<u>Context</u>:
{info:title=Resolution of BRIN}
A ```BRIN``` had been identified in application containing a ```data-test``` module : running ```database:compare-from-prod``` goal on theses applications led to a failure because the ```data-test``` resource wasn't found.
{info}

<u>Description</u>:
The ```database:compare-from-prod``` goal is executed by a ```MavenCommand``` set in reactor mode.
Now, when in this mode, the build is done in a separate process, which solves the problem encountered with ```database:compare-from-prod``` goal.

<u>Example</u>: clean install in reactor mode
```java
MavenCommand installCommand;
File checkoutDirectory;
...
installCommand.execute(new String[[]]{"clean", "install"},
                       checkoutDirectory,
                       getLog(),
                       true); // set the build in reactor mode
```