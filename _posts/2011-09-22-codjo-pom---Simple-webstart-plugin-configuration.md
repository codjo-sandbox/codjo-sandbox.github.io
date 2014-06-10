---
layout: post
title: agf-pom - Simple-webstart-plugin configuration
tags: [framework-1-212,codjo-pom]
---
<u>Context :</u>
As jdk15_06 is not windows seven compatible, java applications need to specify specific deployment system properties in their jnlp (e.g. user.timezone, sun.java2d.noddraw).

see : [[framework:/2011/09/16/codjo-pom - Upgrade simple-webstart-plugin]]

<u>Description :</u>
Delreco has been configured to fill these system properties using the new ```deploymentProperties```.

codjo-pom has been configured:
```
	<plugin>
	    <groupId>org.bud.maven.mojo</groupId>
	    <artifactId>maven-simplewebstart-plugin</artifactId>
	    <configuration>
	        <jnlp>
	            <codebase>@jnlpCodebase@</codebase>
	            ....
	        </jnlp>
	        <resourcesAddOn>@deploymentProperties@</resourcesAddOn>    
	    </configuration>
			...
	</plugin>                        
```
