---
layout: post
title: agf-test - Optimisation de AssertVisible lorsque expected="false"
tags: [codjo-test,framework-1-33]
---
Auparavant, l'exécution du ```AssertVisible``` avec l'attribut ```expected``` à ```false``` mettait 15 secondes à s'exécuter (le délai fixé pour le ```timeout``` pour cette balise), puisqu'il faisait une recherche du composant le temps du ```timeout```.\\ \\ Maintenant, l'exécution dans ces mêmes conditions se fait quasi-instantanément, et dans le cas du ```WaitingPanel``` (comme tout autre composant visible lors de l'exécution de cette balise), ce même timeout sera pris en compte.