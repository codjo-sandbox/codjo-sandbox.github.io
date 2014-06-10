---
layout: post
title: agf-test - Extension de la balise assertTable
tags: [framework-1-28,codjo-test]
---
Mise en place d'un mécanisme permettant d'étendre le comportement par défaut de la balise ```<assertTable>```.
Cela permet d'avoir une assertion spécifique à un type de table ou à un type de renderer.

### Cas d'utilisation :

- un renderer renvoyant un composant spécifique autre que les ```JLabel``` et ```JCheckBox```.
- un renderer "classique" sur lequel l'assert est inhabituel. Ex : un ```JLabel``` dont l'assert porte sur l'icône et non sur le texte.

### Exemple :

```
public class DummyTableTestBehavior implements AssertTableDescriptor {

    public void assertTable(JTabe table, AssertTableStep step) {
        int row = step.getRow();
        int column = TableTools.searchColumn(table, step.getColumn());
        String currentValue = (String) table.getValueAt(row, column);

        if(!currentValue.startsWith(expected)) {
            throw new GuiConfigurationException(
                "La valeur de la cellule '" <u> currentValue </u> "' doit commencer par " + expected);
        }
    }
}
```