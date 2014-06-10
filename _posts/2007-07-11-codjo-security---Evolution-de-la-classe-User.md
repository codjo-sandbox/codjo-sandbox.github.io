---
layout: post
title: agf-security - Evolution de la classe User
tags: [codjo-security,framework-1-4]
---
Ajout sur la classe ```User``` des méthodes suivantes permettant d'obtenir l'identifiant de l'utilisateur, et de savoir si un utilisateur appartient à un groupe particulier.

```java
public UserId getId();

public boolean isInRole(String roleId);
```
