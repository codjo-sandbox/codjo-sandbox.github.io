---
layout: post
title: agf-datagen - Ajout de la possibilité de spécifier la requête SQL pour un handler update
tags: [codjo-datagen,framework-1-50]
---
Il est maintenant possible de spécifier la requête SQL utilisée par un handler update.

<u>Exemple</u> de configuration d'un handler update sur une table ne contenant que 2 colonnes.
```xml
<handler-update id="updateDividend">
  <query>{call sp_Mint_UpdateDividend(@DIVIDEND_ID=?,@CREATED_BY=?)}</query>
</handler-update>
```

**NB** : Les valeurs (i.e. les '?') doivent être déclarées dans le même ordre que les ```fields``` définies dans l'entité datagen.

