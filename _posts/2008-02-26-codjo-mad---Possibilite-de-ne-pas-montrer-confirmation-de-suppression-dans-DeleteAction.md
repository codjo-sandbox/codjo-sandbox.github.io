---
layout: post
title: agf-mad - Possibilité de ne pas montrer confirmation de suppression dans DeleteAction
tags: [codjo-mad,framework-1-32]
---
Ajout de la possibilité de ne pas montrer la fenêtre de confirmation dans le DeleteAction.
Pour cela il suffit d'utiliser la nouvelle méthode dans ```RequestToolbar```:

```setDeleteConfirmMessage(null);```

La méthode peut être appelée depuis la RequestToolbar ou bien depuis l'action même.