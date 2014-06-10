---
layout: post
title: agf-segmentation - Added possibility to use joins in the delete configuration of a family
tags: [framework-1-191,codjo-segmentation,hot-topics]
---
<u>Context</u>
The configuration of the deletion step of previous segmentation results would only allow a where clause to be specified:

```xml
  <delete-config>
    <where-clause>PERIOD = '$period$' and CLASSIFICATION_ID = $segmentationId$</where-clause>
  </delete-config>
```

<u>Description</u>
A table join was needed to be more specific in the deletion step, so the ```join-key``` element has been added as a possible child (0 to multiple occurences) to the ```delete-config``` tag:

```xml
  <delete-config>
    <where-clause><![CDATA[
    AP_SLEEVE_OUTSTAND.PERIOD between '$period$' and '$endPeriod$'
    and AP_SLEEVE_OUTSTAND.CLASSIFICATION_ID = $segmentationId$
    and (0 = $isRestricted$ or (1 = $isRestricted$ and AP_OUTSTAND.IS_RESTRICTED = 1))
    ]]></where-clause>
    <join-key left="AP_SLEEVE_OUTSTAND" type="inner" right="AP_OUTSTAND">
      <part left="PERIOD" operator="=" right="PERIOD"/>
      <part left="SECURITY_ID" operator="=" right="SECURITY_ID"/>
      <part left="STRATEGIC_TYPE" operator="=" right="STRATEGIC_TYPE"/>
      <part left="PORTFOLIO_CODE" operator="=" right="PORTFOLIO_CODE"/>
    </join-key>
  </delete-config>
```

See: [[Documentation codjo-segmentation]]