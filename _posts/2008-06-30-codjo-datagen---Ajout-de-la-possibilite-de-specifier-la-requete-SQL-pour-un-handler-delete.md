---
layout: post
title: agf-datagen - Ajout de la possibilité de spécifier la requête SQL pour un handler delete
tags: [codjo-datagen,framework-1-50]
---
Il est maintenant possible de spécifier la requête SQL utilisée par un handler delete.

<u>Exemple</u> de configuration d'un handler delete sur une table ne contenant que 2 colonnes.
```xml
<handler-delete id="deleteDividend">
  <query>{call sp_Mint_DeleteDividend(@DIVIDEND_ID=?,@BEGIN_DATE=?)}</query>
</handler-update>
```

**NB** : Les valeurs (i.e. les '?') doivent être déclarées dans le même ordre que les ```primary-key``` définies dans l'entité datagen.
