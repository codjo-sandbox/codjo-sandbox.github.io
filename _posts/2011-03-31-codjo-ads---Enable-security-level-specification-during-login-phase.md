---
layout: post
title: agf-ads - Enable security level specification during login phase
tags: [framework-1-193,codjo-ads]
---
<u>Context</u>
There are two kinds of security level in ADS : 0 and 1. Security level 0 should be dedicated
to batch clients (no need to renew the password every three month), and security level 1 to gui clients (need to renew password every three month).

<u>Description</u>
Actually, all authentications through ADS are made with security level 1. It implies that batch users like ```user_ksl``` and ```user_batch``` have to renew their password every three month. Now, one has to provide the security level while connecting to ADS.


Here's the new login method signature in ```AdsService```:

```
 public UserToken login(String login, String password, int securityLevel)
          throws AdsSystemException, AccountLockedException {
...
}
```


{warning:title=Warning}
Since login method signature has changed, backward compatibility is broken.
Impacts can be seen on : 
 - codjo-security
 - magic
{warning}