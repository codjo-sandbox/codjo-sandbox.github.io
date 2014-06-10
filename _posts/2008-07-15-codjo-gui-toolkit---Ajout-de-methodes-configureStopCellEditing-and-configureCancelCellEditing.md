---
layout: post
title: agf-gui-toolkit - Ajout de méthodes configureStopCellEditing and configureCancelCellEditing
tags: [codjo-gui-toolkit,framework-1-52]
---
Les méthodes _configureStopCellEditing_ (resp. _configureCancelCellEditing_) permettent de configurer la gestion du _stopCellEditing_ (resp. _cancelCellEditing_) entre une JTable et un ensemble de boutons.
Exemple :
```
TableUtil.configureStopCellEditing(aTable, validateButton, ...);
TableUtil.configureCancelCellEditing(aTable, cancelButton, ...);
```
Ainsi, lorsque l'utilisateur saisira une donnée dans une cellule puis cliquera sur l'un de ces boutons, la table stoppera (ou annulera) l'édition de celle-ci.
\\
{note:title=Important}
Si des **ActionsListeners** ont été ajoutés pour des besoins spécifiques alors les méthodes ci-dessus doivent être appliquées en "dernier". Cela s'explique par le fait que les listeners sont exécutés dans l'ordre inverse (le plus récent au plus ancien) et donc le _stop/cancelCellEditing_ ne serait pas exécuté au bon moment s'il n'était pas ajouté en dernier.
{note}