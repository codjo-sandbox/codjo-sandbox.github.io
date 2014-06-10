---
layout: post
title: agf-mad - Correction problème activation du bouton enregistrer
tags: [framework-1-59,codjo-mad]
---
Dans le ButtonPanelLogic, lorsque l'option closeOnSave est à faux, l'activation et la désactivation du bouton enregistrer n'étaient pas correctement gérées.

Fonctionnement avant correction :
- Modification d'un champ (cochage d'une checkBox)
- Activation du bouton Enregistrer (pour que l'on puisse enregistrer la modification)
- Sauvegarde (Donc en base checkBox à true)
- Bouton Enregistrer toujours actif.
- Retour arrière sur la modification (soit décochage du checkBox)
- Grisage du bouton "Enregistrer"
=> Pour pouvoir ré-enregistrer la checkBox à false, il faut fermer l'écran et le rouvrir.

Fonctionnement après correction :
- Modification d'un champ (cochage d'une checkBox)
- Activation du bouton Enregistrer (pour que l'on puisse enregistrer la modification)
- Sauvegarde (Donc en base checkBox à true)
- **Bouton Enregistrer grisé**.
- Retour arrière sur la modification (soit décochage du checkBox)
- **Activation du bouton Enregistrer**