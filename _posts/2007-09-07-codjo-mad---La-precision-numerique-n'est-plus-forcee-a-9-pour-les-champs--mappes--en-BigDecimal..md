---
layout: post
title: agf-mad - La précision numérique n'est plus forcée à 9 pour les champs "mappés" en BigDecimal.
tags: [codjo-mad,framework-1-11]
---
Elle était forcée à 9, ce qui générait une exception lors de la saisie de nombres décimaux avec plus de 9 chiffres après la virgule (dans les fenêtres de détails par exemple).\\ \\