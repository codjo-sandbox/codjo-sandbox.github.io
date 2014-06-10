---
layout: post
title: agf-datagen - Génération de la balise entity dans le fichier referential-preference.xml
tags: [codjo-datagen,framework-1-93]
---
La génération du fichier de préférences dont se nourrit codjo-referential a été enrichie de la balise ```entity```. Elle est variabilisée à l'aide du nom de la classe propre à l'entité datagen.

```title=Exemple de code généré
<preference id="CountryList"
                detailWindowClassName="com.agf.referential.gui.ReferentialDetailLogic">
        <entity>Country</entity>
...
</preference>
```

Cela permet automatiquement de tenir compte du nombre maximum de caractères des champs et de savoir si ces champs sont requis au niveau des écrans détails.