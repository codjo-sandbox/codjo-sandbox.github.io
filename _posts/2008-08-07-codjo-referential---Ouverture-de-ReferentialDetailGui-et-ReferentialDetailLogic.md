---
layout: post
title: agf-referential - Ouverture de ReferentialDetailGui et ReferentialDetailLogic
tags: [codjo-referential,framework-1-56,hot-topics]
---

<table style='background-color: #FFFFCE;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/warning.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>
La solution ci-dessous est temporaire, en attendant que le gourou Bobo revienne ... ;)
</p></td>
          </tr>
</table>

Dans MINT, la colonne d'un référentiel pointe vers un autre référentiel. La contrainte de clé n'existant pas pour certaines problématiques spécifiques à MINT, l'utilisation d'un **GuiCustomizer** pour générer une ComboBox correspond au besoin.

La visibilité des classes **ReferentialDetailGui** et **ReferentialDetailLogic** a été modifiée afin de pouvoir utiliser son propre GuiCustomizer pour un référentiel donné.

Le principe est le suivant :
1. Surcharger les préférences du référentiel concerné en spécifiant une autre logic dans l'attribut **detailWindowClassName** en créant un fichier de préférence (à mettre dans /conf):
```xml
<preferenceList>
    <preference id="ExecuteValuationList" detailWindowClassName="com.agf.mint.gui.referential.ExecuteValuationDetailLogic">
        ...
    </preference>
</preferenceList>
```
1. Charger le fichier de préférences est chargé à travers un **GuiPlugin** :
```
public class MintReferentialGuiPlugin extends AbstractGuiPlugin {

    private static final String PREFERENCES_OVERRIDEN_FILE = "referential-preferences-overriden.xml";

    private MadGuiPlugin madGuiPlugin;


    public MintReferentialGuiPlugin(MadGuiPlugin madGuiPlugin)
          throws IOException {
        this.madGuiPlugin = madGuiPlugin;
    }


    @Override
    public void initGui(GuiConfiguration configuration) throws Exception {
        PreferenceFactory.initFactory();
        if (PreferenceFactory.containsPreferenceId("ExecuteValuationList")) {
            this.madGuiPlugin.getConfiguration().addPreferenceMapping(PREFERENCES_OVERRIDEN_FILE);
        }
    }
}
```
1. Déclarer le GuiPlugin dans la classe principal du module Gui de l'application :
```
public static void main(String[[]] arguments) throws IOException {
        final MadGuiCore guiCore = new MadGuiCore();

        ...
        guiCore.addPlugin(MintReferentialGuiPlugin.class);
        ...
    }
```
1. Ecrire la classe **com.agf.mint.gui.referential.ExecuteValuationDetailLogic** qui héritera de **ReferentialDetailLogic** avec le GuiCustomizer qui va bien:
```
public class ExecuteValuationDetailLogic extends ReferentialDetailLogic {

    public ExecuteValuationDetailLogic(DetailDataSource dataSource, String title, Map<String, Field> fieldMap)
          throws Exception {
        super(dataSource, createGui(title, fieldMap));
    }


    private static ReferentialDetailGui createGui(String title,
                                           Map<String, Field> fieldMap)
          throws Exception {
        return new ReferentialDetailGui(title, fieldMap, new ExecuteValuationCustomizer());
    }


    private static class ExecuteValuationCustomizer implements GuiCustomizer {

        public boolean handle(Field field) {
            return "valFrequency".equals(field.getName());
        }


        public JComponent createGui(Field field) {
            RequestComboBox requestComboBox = new RequestComboBox();
            requestComboBox.initRequestComboBox("refCode", "refLabel", !field.isRequired());
            field.setComponent(requestComboBox);
            return requestComboBox;
        }


        public void declareField(DetailDataSource dataSource, Field field) {
            dataSource.declare(field.getName(), field.getComponent());
            ...
        }
        ...
    }
```