---
layout: post
title: maven-database-plugin - Wrong agf-test dependency scope
tags: [framework-1-172,maven-database-plugin]
---
<u>Context</u>:
After recent framework modifications (see. [[framework:/2010/10/22/codjo-pom - New Library jxls available] and [/2010/10/26/agf-test - Upgrade of class ExcelUtil]]), a unit test failed:
```
org.apache.maven.plugin.MojoExecutionException: Missing:
----------
1) javax.servlet:servlet-api:jar:2.3

  Try downloading the file manually from the project website.

  Then, install it using the command: 
      mvn install:install-file -DgroupId=javax.servlet -DartifactId=servlet-api \
          -Dversion=2.3 -Dpackaging=jar -Dfile=/path/to/file

  Path to dependency: 
  	1) com.agf.maven.mojo:maven-database-plugin:maven-plugin:1.48-SNAPSHOT
  	2) com.agf.test:codjo-test-common:jar:3.56-SNAPSHOT
  	3) org.apache.poi:poi:jar:3.6
  	4) commons-logging:commons-logging:jar:1.1
  	5) javax.servlet:servlet-api:jar:2.3

----------
1 required artifact is missing.
```

<u>Description</u>:
```maven-database-plugin``` had a dependency to ```codjo-test``` with ```scope compile```. It has been modified to ```scope test```.
