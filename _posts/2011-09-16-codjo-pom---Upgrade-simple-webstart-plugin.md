---
layout: post
title: agf-pom - Upgrade simple-webstart-plugin
tags: [framework-1-211,codjo-pom,hot-topics]
---
<u>Context :</u>
Since jdk15_06 is not windows seven compatible, java applications need to specify specific deployment system properties in their jnlp (e.g. user.timezone, sun.java2d.noddraw).

<u>Description :</u>
In maven-simplewebstart-plugin version 0.5, a new tag ```resourcesAddOn``` has been added in configuration tag to allow free text insertion under properties tag in jnlp.

Delreco will be configured to fill it with the deployment properties required for Windows seven:

<u>Example</u>: 

codjo-pom configuration 
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

Delreco configuration (for template resolution):
```
deploymentProperties = 
                       <property name="user.timezone" value="Europe/Paris"/>
		      <property name="sun.java2d.noddraw" value="true"/>
```