---
layout: post
title: agf-sql - Order by fields can be defined when generating Select queries
tags: [framework-1-175,codjo-sql,api-change,codjo-broadcast,codjo-segmentation]
---
<u>Context</u>
```SelectQueryBuilder``` does not allow to define "order by" fields to be generated in the final ```select``` query.

<u>Description</u>
The ```QueryConfig``` interface now allows to define "order by" fields via the ```getOrderByFields``` method.

```
public interface QueryConfig {
...
  OrderByField[[]] getOrderByFields();
...
}
```

<u>Example</u>
```

   SelectQueryBuilder builder = new SelectQueryBuilder(new QueryConfig() {
   ...
       public OrderByField[[]] getOrderByFields() {
                return new OrderByField[[]]{
                      new OrderByField("AP_MATABLE", "MY_FIELD1"),
                      new OrderByField("AP_MATABLE", "MY_FIELD2")
                };
            }
    });

```