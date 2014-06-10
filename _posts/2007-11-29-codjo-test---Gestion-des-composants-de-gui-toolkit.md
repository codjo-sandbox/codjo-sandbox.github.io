---
layout: post
title: agf-test - Gestion des composants de gui-toolkit
tags: [codjo-gui-toolkit,codjo-test,framework-1-22,hot-topics]
---
Un mécanisme d'extension des comportements des différentes balises disponibles dans les tests release a été mis en place dans codjo-test.

Désormais les composants non swing peuvent être assortis d'une classe ```MonComposantTestBehavior``` implémentant l'interface ```SetValueBehavior``` surchargeant les méthodes du step associée à la balise ```<setValue>``` de test release.
Cette classe doit se trouver dans le même package que la classe du composant principal (idéalement, dans le jar de test uniquement).

La gestion des composants graphiques définis dans gui-toolkit a été modifiée et rendue complètement générique dans codjo-test. Ainsi, la classe ```DateField``` a été mise à jour en utilisant cette mécanique et peut servir d'exemple :
```
public class DateFieldTestBehavior implements SetValueDescriptor {

    public void setValue(Component comp, SetValueStep step) {
        String value = step.getValue();
        try {
            Date date = DateUtil.createDate(value);
            comp.requestFocus();
            ((DateField)comp).setDate(date);
        }
        catch (ParseException e) {
            throw new GuiConfigurationException(
                value + " n'est pas une date valide. Utiliser le format yyyy-MM-dd");
        }
    }
}
```
Pour l'instant, seul le descripteur pour la balise ```setValue``` est disponible et peut être étendus à des composants spécifiques.

<table style='background-color: #FFCCCC;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/forbidden.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>A la suite de la mise à jour de la classe ```DateField``` dans gui-toolkit, **il est maintenant indispensable d'ajouter une dépendance vers la lib gui-toolkit dans le module test-release** des applications concernées.
Ajoutez les lignes suivantes dans le ```pom.xml``` du module test-release :
```
<dependencies>
    ...
    <dependency>
        <groupId>com.agf.gui-toolkit</groupId>
        <artifactId>codjo-gui-toolkit</artifactId>
        <classifier>tests</classifier>
    </dependency>
</dependencies>
```</p></td>
          </tr>
</table>
