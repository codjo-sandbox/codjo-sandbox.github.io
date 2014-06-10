---
layout: post
title: agf-segmentation - Customisation de la gestion d'erreur lors de la sauvegarde d'une poche
tags: [codjo-segmentation,framework-1-116]
---
Sur l'écran détail d'un axe, un ```DataLink``` est utilisé entre la ```DataSource``` de l'axe édité et la ```DataSource``` des poches correspondantes.

La méthode suivante a été ajoutée pour changer l'objet ```ErrorHandler``` dans ce DataLink :

```
public void setAxisSleevesLinkErrorHandler(ErrorHandler handler)
```