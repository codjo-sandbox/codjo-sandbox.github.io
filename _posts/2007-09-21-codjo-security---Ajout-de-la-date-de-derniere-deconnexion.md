---
layout: post
title: agf-security - Ajout de la date de dernière déconnexion
tags: [codjo-security,framework-1-13]
---
Ajout de la date de dernière déconnexion sur le profil de l'utilisateur. Cette information est maintenant accessible par code via le service de sécurité.

<u>Exemple :</u>
```java
UserData user = getSecurityService().getUserData(userId, "bruce");

user.getLastLogin();
user.getLastLogout();

```

