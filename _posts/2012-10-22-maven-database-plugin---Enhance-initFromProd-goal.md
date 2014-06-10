---
layout: post
title: maven-database-plugin - Enhance initFromProd goal
tags: [maven-database-plugin,framework-2-37]
---
<u>Context</u>
Database comparison is not implemented for Oracle database.

<u>Description</u>
Until the implementation of Oracle database comparison, we added the ability to execute the sql release script in the ```database:init-from-prod``` goal (it is possible to use oracle tool to make a diff between databases).

``` mvn database:init-from-prod -DrunReleaseScripts=true ```

see : [[documentation|framework:maven-database-plugin - init-from-prod]]

<u>Example of how to override the goal executed during the integration process</u>
In the project ```pom.xml``` you have to define the following profile
```xml
        <profile>
            <id>process-integration</id>
            <activation>
                <property>
                    <name>process</name>
                    <value>integration</value>
                </property>
            </activation>
            <build>
                <pluginManagement>
                    <plugins>
                        <plugin>
                            <groupId>net.codjo.maven.mojo</groupId>
                            <artifactId>maven-database-plugin</artifactId>
                            <executions>
                                <execution>
                                    <id>pre-integration-test</id>
                                    <phase>none</phase>
                                </execution>
                                <execution>
                                    <id>override-super-pom-pre-integration-test</id>
                                    <phase>pre-integration-test</phase>
                                    <goals>
                                        <goal>init-from-prod</goal>
                                    </goals>
                                </execution>
                            </executions>
                            <configuration>
                                <runReleaseScripts>true</runReleaseScripts>
                            </configuration>
                        </plugin>
                    </plugins>
                </pluginManagement>
            </build>
        </profile>
```