---
layout: post
title: agf-mad - Validation de l'édition d'une RequestTable à la perte du focus de la table
tags: [codjo-mad]
---
Lorsqu'une ```RequestTable``` est en édition et que l'utilisateur ne valide pas sa saisie en passant sur un autre composant (perte de focus de la RequestTable), alors l'édition de la ```RequestTable``` est soit validée (si la saisie est valide) soit annulée (si la saisie n'est pas valide).

{info:title=Intérêt}Cela évitera notamment de pouvoir être en édition sur plusieurs tables sur des écrans tels que la saisie du tracking GABI.
{info}