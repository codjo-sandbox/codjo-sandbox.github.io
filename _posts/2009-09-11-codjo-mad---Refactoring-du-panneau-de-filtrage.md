---
layout: post
title: agf-mad - Refactoring du panneau de filtrage
tags: [framework-1-113,codjo-mad]
---
La classe ```FilterPanel``` a été refactorée pour en simplifier l'implémentation et l'API.

Un flag ```postponedLoad``` a été rajouté pour permettre de ne pas charger les filtres de type ```RequestComboBox``` lors de l'ajout au panneau de filtrage. Cela permet à l'utilisateur de retarder le chargement après initialisation complète du panneau, ou de le prendre à sa charge entièrement.

La [[documentation|codjo-mad - Utilisation]] a été mise à jour.