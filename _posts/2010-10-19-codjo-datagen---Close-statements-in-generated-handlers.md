---
layout: post
title: agf-datagen - Close statements in generated handlers
tags: [framework-1-171,codjo-datagen]
---
<u>Context :</u>
Calls to setters weren't embedded in a try-catch block (see: [[framework:/2010/09/02/codjo-datagen - Close statements in generated handlers]])

<u>Description :</u>
By now, the generated handler's code looks like the following example.

```
private void executeDatabaseUpdate(Connection connection, String querySql, smartHolding obj) throws SQLException {
        CallableStatement query = connection.prepareCall(querySql);
        try {
            query.setString
              (1, obj.getAccountingCurrencyCode());
            query.setString
              (2, obj.getAssetOrCash());
            query.setString
              (3, obj.getDataSourceCode());
            query.setString
              (4, obj.getInstrId());
            query.execute();
        } finally {
            query.close();
        }
    }

```