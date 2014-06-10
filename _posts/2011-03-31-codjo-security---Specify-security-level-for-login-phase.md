---
layout: post
title: agf-security - Specify security level for login phase
tags: [hot-topics,framework-1-193,codjo-security]
---
<u>Context</u>
There are two kinds of security level in ADS : 0 and 1. Security level 0 should be dedicated
to batch clients (no need to renew the password every three month), and security level 1 to gui clients (need to renew password every three month).

see: [[framework:/2011/03/31/codjo-ads - Enable security level specification during login phase]]

<u>Description</u>
Actually, each security client uses security level 1 authentication. 
Since login method has changed in ```codjo-ads```, each client has now to provide a security level value to login.
Now, by default, every client using ```SecurityClientPlugin``` will use security level 0 authentication (```SecurityLevel.SERVICE```). 
The ```SecurityGuiPlugin``` uses security level 1 authentication (```SecurityLevel.USER```).

To allow a plugin to connect with ```SecurityLevel.USER```, one should use ```SecurityLevelHelper``` to add a parameter in the ```containerConfig```


```
//Enable Security level 1 authentication 
SecurityLevelHelper.setSecurityLevel(containerConfiguration, SecurityLevel.USER);

//Enable Security level 0 authentication (by default)
SecurityLevelHelper.setSecurityLevel(containerConfiguration, SecurityLevel.SERVICE);
```


{warning:title=Warning}
Since login method signature in ```SecurityServiceHelper``` has changed, backward compatibility is broken.
Impacts can be seen on : 
 - codjo-standalone-client
 - mint
 - benchmark
{warning}