---
layout: post
title: agf-broadcast - renderer sur ComboBox de la famille (Section)
tags: [codjo-broadcast,framework-1-34]
---
Un renderer a été positionné sur la ComboBox de la famille sur l'écran détail concernant la section (classe ```BroadcastSectionsDetailWindow``` ). Ce renderer s'appuie sur la méthode getFamilyLabel() ajoutée à l'interface ```GuiPreferences```. Cette méthode est implémentée dans la classe ```AbstractGuiPreferences``` de façon à renvoyer l'identifiant de la famille (compatibilité ascendante).

Il est donc possible de surcharger cette méthode de façon à avoir un libellé associé à l'identifiant de la famille.
```java

public class MyGuiPreferences extends AbstractGuiPreference {
...
    @Override
    public String getFamilyLabel() {
        return "Libellé " + getFamily();
    }
...
}
```