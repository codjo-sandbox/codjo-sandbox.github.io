---
layout: post
title: agf-gui-toolkit - Correction sur le FeedbackPanel
tags: [framework-1-95,codjo-gui-toolkit]
---
Le ```FeedbackPanel``` fonctionnait correctement dans le contexte particulier pour lequel il avait été développé initialement (à savoir ```SMART```) mais souffrait de problèmes lorsqu'il était utilisé dans un autre contexte (```MINT``` notamment).

Le bug, dû à des comportements swing différents d'une application à une autre a été corrigé.
