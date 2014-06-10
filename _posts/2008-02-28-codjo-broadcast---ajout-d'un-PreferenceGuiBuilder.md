---
layout: post
title: agf-broadcast - ajout d'un PreferenceGuiBuilder
tags: [codjo-broadcast,framework-1-33]
---
Introduction de la notion de ```PreferenceGuiBuilder``` : ce builder construit des préférences paramétrés.

<u>Exemple de PreferenceGuiBuilder</u> : 
```java
private static class ReferentialGuiPreferenceBuilder implements GuiPreferenceBuilder {
     private final String familyId;


     ReferentialGuiPreferenceBuilder(String familyId) {
         this.familyId = familyId;
     }


     public GuiPreference createPreference(GuiConfiguration guiConfiguration) throws Exception {
         return new ReferentialGuiPreferences(familyId, guiConfiguration.getStructureReader());
     }
}
```

<u>Exemple de configuration</u> : 
```java
BroadcastGuiPlugin plugin = ...
plugin.getConfiguration().addGuiPreference(new ReferentialGuiPreferenceBuilder("CURRENCY"));
```
