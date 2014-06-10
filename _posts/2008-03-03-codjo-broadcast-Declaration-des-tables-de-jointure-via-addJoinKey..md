---
layout: post
title: agf-broadcast Déclaration des tables de jointure via addJoinKey.
tags: [codjo-broadcast,framework-1-33,hot-topics]
---
Les deux méthodes getTableLabels() et getTableNames() ont été supprimées de l'interface GuiPreference
et seront déclarées final sur la classe AbstactGuiPreference lors d'une prochaine version.


exemple de code à remplacer dans les projets :

```java
public String[[]] getTableNames() {
   return new String[[]] {"AP_BRANCH_CODIFICATION", "#COMPUTED_ACC_ENTRY", 
"AP_INDIRECT_FEES as dei","AP_INDIRECT_FEES as dsi"};
}
 
public Map getJoinKeyLabels() {
    return getTableLabels();
}
```

Création de la méthode addJoinKey(String tableName, String tableLabel) et addJoinKey(String tableName) pour l'initialisation des tables de jointures au niveau client.

```java
@Override
    protected void initJoinKeys() {
        addJoinKey(getComputedTableName());
        addJoinKey("AP_BRANCH_CODIFICATION");
        addJoinKey("AP_INDIRECT_FEES as dei", "Droits d'entrées indirects");
        addJoinKey("AP_INDIRECT_FEES as dsi", "Droits de sorties indirects");
    }
```

   