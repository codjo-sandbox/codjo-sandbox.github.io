---
layout: post
title: agf-tokio - Ajout de la balise group
tags: [framework-1-105,codjo-tokio,hot-topics,kaizen-tr]
---
{info:title=Dans le cadre du Kaizen TR}{info}
Il est maintenant possible dans un fichier tokio de spécifier des groupes dans les "input" et les "output".
Ces groupes permettent simplement de regrouper des données afin d'améliorer la lisibilité.

<u>Exemple</u> :
```
<input>
  <group name="un groupe fonctionnel de données">
    <AP_TABLE1>
      <row>
        (...)
      </row>
    </AP_TABLE1>
    <AP_TABLE2>
      <row>
        (...)
      </row>
    </AP_TABLE2>
  </group>
        
  <AP_TABLE1>
    <row>
      (...)
    </row>
  </AP_TABLE1>
</input>
```