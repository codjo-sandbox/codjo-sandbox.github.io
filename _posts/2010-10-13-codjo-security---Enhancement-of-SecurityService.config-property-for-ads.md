---
layout: post
title: agf-security - Enhancement of SecurityService.config property for ads
tags: [framework-1-170,codjo-security,safe,framework-1-170-1]
---
<u>Context</u>:
* Security parameters to use ```ADS``` were not clearly readable. Some improvement to manage this configuration was required.
* Backup server had to be configured.

<u>Description</u>:
Specific ```ADS``` configuration has been made.
Applications must still have configured:
```title=server-config.properties

SecurityService.config = @securityServiceConfig@

```

Delreco configuration will have:
```

securityServiceConfig = ads:application.user=<APPLICATION_USER>|\
                            application.pwd=<APPLICATION_PASSWORD>|\
                            project.name=<PROJECT_NAME>|\
                            ldap.url=<LDAP_URL>|\
                            ssl.url=<SSL_URL>|\
                            ldap.url.backup=<LDAP_URL_BACKUP>|\
                            ssl.url.backup=<SSL_URL_BACKUP>|\
                            project.base=<PROJECT_BASE>|\
                            role.base=<ROLE_BASE>|\
                            permission.base=<PERMISSION_BASE>|\
                            user.base=<USER_BASE>|\
                            adsbv.jnlp.url=<ADSBV_JNLP_URL>

```

see: [[framework:Mise en place de codjo-security#Paramétrage ADS]]