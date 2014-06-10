---
layout: post
title: agf-jconnect - Bug fix on setObject with numeric
tags: [framework-1-122,codjo-jconnect]
---
<u>Context</u>:
The following statement raised the following error "_La conversion implicite du type de donnée 'CHAR' en 'NUMERIC' n'est pas autorisée. Employez la fonction CONVERT pour exécuter cette interrogation._":
```java
  preparedStatement.setObject(1, "11.11", Types.NUMERIC)
```

<u>Description</u>:
This bug was due to the ```codjo-jconnect``` wrapper, it has been fixed.
