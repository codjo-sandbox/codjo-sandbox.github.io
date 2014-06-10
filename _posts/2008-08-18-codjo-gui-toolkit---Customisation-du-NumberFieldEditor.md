---
layout: post
title: agf-gui-toolkit - Customisation du NumberFieldEditor
tags: [framework-1-57,codjo-gui-toolkit]
---
Il est à présent possible de customiser le ```NumberField``` affiché dans un ```NumberFieldEditor```. Il suffit pour cela de surcharger la méthode ```customizeEditor(NumberField editor)```.

Exemple :
```
    public class CustomizedNumberEditor extends NumberFieldEditor {
        @Override
        protected void customizeEditor(NumberField zeEditor) {
            zeEditor.setRenderer(new NumberFieldRenderer(
                  new DecimalFormat("##0.###", new DecimalFormatSymbols(Locale.ENGLISH))));
            zeEditor.setApplyRendererInEditMode(true);
        }
    }
```