---
layout: post
title: agf-mad - API change in SqlHandler class
tags: [framework-1-130,codjo-mad]
---
<u>Context:</u>
Damas users need to manage tables without primary keys.

<u>Description:</u>
It was necessary to change ```getPrimaryKeys``` method's visibility in ```SqlHandler``` class.
By now, this method is in the protected scope (instead of private).

<u>Example:</u>
```
public class GenericUpdateHandler extends AbstractGenericHandler {
    private Map<String, String> primaryKeyFields;

    @Override
    public String proceed(Node node) throws HandlerException {
        try {
            primaryKeyFields = getPrimaryKeyFields(node);
            return super.proceed(node);
        }
        catch (Exception ex) {
            throw new HandlerException(ex);
        }
    }
    @Override
    protected void fillQuery(PreparedQuery query, Map<String, String> arguments) throws SQLException {
        // build the first part of the update query
        ............

        // use the primaryKeyFields to build  where clause of update query
        for (TableField field : getPrimaryField(table)) {
            //noinspection unchecked
            query.setObject(index<u></u>, primaryKeyFields.get(field.getName()), ...));
        }
    }
}

```