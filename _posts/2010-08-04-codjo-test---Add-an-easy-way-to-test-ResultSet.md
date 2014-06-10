---
layout: post
title: agf-test - Add an easy way to test ResultSet
tags: [framework-1-158,codjo-test]
---
<u>Context</u>
We need to unitary test results that come from an SQL request.

<u>Description</u>
A new method ```AssertUtil.assertResultSetRow(String[[][]], ResultSet)``` is now available.

<u>Example</u>
```
@Test
public void shouldFindAllChanges() throws Exception {
  tokio.insertInputInDb("nominal");

  ResultSet changes = ChangesUtil.findAllChanges(tokio.getConnection(), "005", "1998-01-01");

  assertTrue(changes.next());

  AssertUtil.assertResultSetRow(new String[[][]]{
    {"STATUS_CODIFICATION_CODE", "005"},
    {"BEGIN_DATE", "9999-01-01"},
    {"TABLE_NAME", "BranchCodification"},
    {"TABLE_VIEW", null},
    {"TABLE_SELECTOR", null},
    {"FIELD_NAME", "sicovamCode"},
  },
    changes);

  assertTrue(changes.next());

  AssertUtil.assertResultSetRow(new String[[][]]{
    {"STATUS_CODIFICATION_CODE", "005"},
    {"BEGIN_DATE", "1998-01-01"},
    {"TABLE_NAME", "SegmentCodification"},
    {"TABLE_VIEW", null},
    {"TABLE_SELECTOR", null},
    {"FIELD_NAME", "directFees"},
  },
    changes);

  assertTrue(changes.next());

  AssertUtil.assertResultSetRow(new String[[][]]{
    {"STATUS_CODIFICATION_CODE", "005"},
    {"BEGIN_DATE", "9999-01-01"},
    {"TABLE_NAME", "RiskProfile"},
    {"TABLE_VIEW", "RiskProfileList"},
    {"TABLE_SELECTOR", "selectAllRiskProfile"},
    {"FIELD_NAME", null},
  },
    changes);

  assertFalse(changes.next());
}

```
