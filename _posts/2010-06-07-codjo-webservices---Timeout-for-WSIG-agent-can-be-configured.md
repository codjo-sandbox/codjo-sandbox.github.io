---
layout: post
title: agf-webservices - Timeout for WSIG agent can be configured
tags: [framework-1-150,codjo-webservices,api-change]
---
<u>Context</u>
Requests coming from Web world are transmitted to Jade agents via a WSIG agent. By default this agent waits 30 seconds before throwing an exception if the target agent does not respond. This timeout is too low sometimes especially when database is heavily loaded.

<u>Description</u>
The ```WebServicePlugin``` plugin can be configured to set a specific timeout in applications, as follows:

```
// timout configuration for 2 minutes
webServicePlugin.getConfiguration().setWSIGTimeout("120000");
```

see [[framework:Mise en place de codjo-webservices]].