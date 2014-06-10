---
layout: post
title: agf-security - Possibilité d'ajouter des backups aux serveurs LDAP
tags: [framework-1-114,codjo-security]
---
Il est possible pour chaque serveur LDAP de spécifier des serveurs de backup.

Il suffit d'ajouter dans le fichier ```server-config.properties``` :

```
...

LdapSecurityService.ldap.backup-servers = domainBackup1, domainBackup2

LdapSecurityService.ldap.domainBackup1.url=ldap://
LdapSecurityService.ldap.domainBackup1.postfix=@postfix

LdapSecurityService.ldap.domainBackup2.url=ldap://
LdapSecurityService.ldap.domainBackup2.postfix=@postfix

LdapSecurityService.ldap._otherDomain1_.backup-servers=domainBackup3

LdapSecurityService.ldap.domainBackup3.url=ldap://
LdapSecurityService.ldap.domainBackup3.postfix=@postfix
```