---
layout: post
title: agf-broadcast - Evolution sur les selectors génériques
tags: [framework-1-104,codjo-broadcast]
---
Ajout de méthodes vides _beforeProceed_ et _afterProceed_ dans _AbstractGenericSelector_ :
```

    protected void beforeProceed (Context context,
                                 Connection connection,
                                 String selectionTableName,
                                 Date broadcastDate)  throws SQLException{
    }


    protected void afterProceed(Context context,
                                Connection connection,
                                String selectionTableName,
                                Date broadcastDate)  throws SQLException{
    }
```