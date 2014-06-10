---
layout: post
title: agf-referential - Suppression du tri pour l'ordre des colonnes dans l'affichage en liste
tags: [framework-1-61,codjo-referential]
---
Le tri des colonnes dans l'affichage amenant les colonnes en première position est supprimé et une personnalisation est possible sur le plugin referentialGuiPlugin .

{<u>}Exemple{</u>} :
```java
public class MyReferentialApplicationPlugin extends AbstractApplicationPlugin {
    public myReferentialApplicationPlugin(ReferentialGuiPlugin referentialGuiPlugin) {
        referentialGuiPlugin.getConfiguration().setListGuiCustomizer(SortColumnListGuiCustomizer.class);
    }
}
// Definition du customizer
public class SortColumnListGuiCustomizer implements ListGuiCustomizer {

    public void handleListOpen(Referential referential, ReferentialListGui listGui) {
        Preference newPreference = new Preference(listGui.getTable().getPreference());
        listGui.getTable().setPreference(sortPreference(newPreference,
                                         getPrimaryKeys(referential)));
    }


    public void handleListClose(ReferentialListGui listGui) {
    }

    public Preference sortPreference(Preference preference, Map<String, Field> pKFieldList) {
        ...
    }
}
```