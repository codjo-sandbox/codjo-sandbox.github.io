---
layout: post
title: agf-datagen - Close statements in generated handlers
tags: [framework-1-163,codjo-datagen]
---
<u>Context :</u>
For SMART project, it was asked to update more than 1000 lines. But in this case, an exceeding cursor number error was obtained from Oracle database.

<u>Description :</u>
By now, the SQL statement used by ```executeDatabaseUpdate``` method of generated updating handlers, are closed.

```
 private void executeDatabaseUpdate(Connection connection, String querySql, smartHolding obj) throws SQLException {
        CallableStatement query = connection.prepareCall(querySql);

        query.setString
              (1, obj.getAccountingCurrencyCode());
        query.setString
              (2, obj.getAssetOrCash());
        query.setString
              (3, obj.getDataSourceCode());
        query.setString
              (4, obj.getInstrId());
        try {
            query.execute();
        } finally {
            query.close();
        }
    }
```