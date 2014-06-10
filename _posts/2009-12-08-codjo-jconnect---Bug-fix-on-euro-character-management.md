---
layout: post
title: agf-jconnect - Bug fix on euro character management
tags: [framework-1-125,codjo-jconnect,hot-topics]
---
<u>Context</u>:
Due to the various configurations of charsets in databases, servers and clients, it was impossible to save and load the euro character from the database.

<u>Description</u>:
A charset converter has been implemented in the library to fix this bug.
This solution fix also the management of these characters:
```java
ÈÉÊ!"#$%&'()*+,-./:;<=>?@[[\]]^_`|}{~¡¢£¤¥¦§¨©ª«¬­®¯°±²³´µ¶·¸¹º»¼½¾¿ÀÁÂÃÄÅÆÇÈÉÊËÌÍÎÏÐÑÒÓÔÕÖ
×ØÙÚÛÜÝÞßàáâãäåæçèéêëìíîïðñòóôõö÷øùúûüýþÿ
```

{info}
Now, it is not necessary to specify the charset and the language on the jdbc connection.
But, if you really want to specify a charset, the language will be set to english (even if you specify french).
{info}

See: [[codjo-jconnect]]