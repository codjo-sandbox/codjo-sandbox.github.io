---
layout: post
title: agf-mad - Added wrapper to internationalize RequestTable
tags: [framework-1-184,codjo-mad]
---
<u>Context</u>
Applications need to be internationalized. Therefore, all framework libraries that expose GUI components or contain messages dedicated to the user have to be internationalized too.

<u>Description</u>
Headers of ```RequestTable``` components have to be internationalizable. A ```InternationalizableRequestTable``` wrapper class has been created to allow the ```RequestTable``` to be notified when the user changes the language.

Keys have to match the "PreferenceName.fieldName" pattern to be taken into account by the i18n mechanism.

<u>Example</u>
```
<preference id="MarketingCountryDate">
  <entity>MarketingCountryDate</entity>
  ...
  <column fieldName="countryCode" label="Code Pays" preferredSize="50"/>
  <column fieldName="marketingStartingDate" label="Date d'autorisation à la commercialisation"/>
    <hidden>
      <column fieldName="classCodificationCode"/>
      <column fieldName="beginDate"/>
    </hidden>
</preference>
```

<u>```i18n.properties```</u>
```
MarketingCountryDate.countryCode=Code Pays
MarketingCountryDate.marketingStartingDate=Date d'autorisation à la commercialisation
```

<u>```i18n_en.properties```</u>
```
MarketingCountryDate.countryCode=Country Code
MarketingCountryDate.marketingStartingDate=Marketing start date
```