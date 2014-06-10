---
layout: post
title: agf-datagen - Add functional key information in structure.xml file
tags: [framework-1-172,codjo-datagen,hot-topics]
---
<u>Context</u>:
On Mint application, we need to retrieve information about functional key for entities that use identity or max generated key.

<u>Description</u>:
In the datagen file, a ```functional-key``` section is added, with the same structure than ```primary-key```.
The ```functional-key``` tag is inherited with the same rules than the ```primary-key``` tag.
In the ```structure.xml``` file, the boolean attribute ```functional-key``` is added.


<u>Example</u>:
```title=Datagen file|type=xml
<entity name="generated.Dividend" table="Q_AP_DIVIDEND" type="quarantine">
        <description>Mon dividend a moi éèçàù</description>

        <feature>
             ...
            <doc-structure/>
            ...
        </feature>

        <primary-key>
            <field name="portfolioCode"/>
            <field name="dividendDate"/>
        </primary-key>

        <functional-key>
            <field name="portfolioCode"/>
            <field name="netDividend"/>
        </functional-key>
...
</entity>
```


```title=Structure file|type=xml
<structure>
        <table type="quarantine" label="Mon dividend a moi" name="Dividend"
               sql="Q_AP_DIVIDEND">
            <field label="Code portefeuille du coupon" name="portfolioCode" sql="PORTFOLIO_CODE"
                   sql-type="varchar" sql-precision="6" sql-required="true" referential="Person"
                   sql-primary-key="true" functional-key="true"/>
            <field label="NET_DIVIDEND" name="netDividend" sql="NET_DIVIDEND" sql-type="numeric"
                   sql-precision="17,2" sql-required="true" referential="Referential"
                   functional-key="true"/>
            <field label="DIVIDEND_DATE" name="dividendDate" sql="DIVIDEND_DATE" sql-type="timestamp"
                   sql-required="true" sql-primary-key="true"/>
        </table>
        ...
</structure>
```