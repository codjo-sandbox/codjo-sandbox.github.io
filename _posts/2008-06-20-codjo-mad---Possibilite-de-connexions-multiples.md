---
layout: post
title: agf-mad - Possibilité de connexions multiples
tags: [codjo-mad,framework-1-49]
---
Il est maintenant possible d'utiliser plusieurs ```MadConnectionPlugin``` simultanément dans la même application. Auparavant les ```MadConnectionOperations``` se basaient sur un singleton, ce qui engendrait des conflits dès lors que plus d'un plugin existait dans la JVM.

```MadConnectionOperations``` utilise maintenant correctement la connexion qui correspond à son plugin.
