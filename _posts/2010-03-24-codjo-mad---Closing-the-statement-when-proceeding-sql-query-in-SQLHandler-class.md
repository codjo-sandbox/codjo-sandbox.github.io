---
layout: post
title: agf-mad - Closing the statement when proceeding sql query in SQLHandler class
tags: [framework-1-139,codjo-mad]
---
<u>Context :</u>
In ```Smart``` project, it was needed to add a multiple edition functionnality.
To implement this functionnality, many update queries had to be proceeded. So, statement objects had to be closed to improve performances.

<u>Description :</u>
In ```SqlHandler``` class, a finally block closes the statement object.

```java
     finally {
          if (statement != null) {
                statement.close();
           }
     }
```