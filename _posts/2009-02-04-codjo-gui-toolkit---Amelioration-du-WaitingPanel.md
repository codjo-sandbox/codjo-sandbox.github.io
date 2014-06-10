---
layout: post
title: agf-gui-toolkit - Amélioration du WaitingPanel
tags: [framework-1-82,codjo-gui-toolkit,hot-topics]
---
Auparavant, le composant ```WaitingPanel``` était lancé même si le temps de traitement était très court ( < à 1 sec). A présent, il se lancera seulement si le traitement prend plus de 1 seconde. Ce délai de 1 seconde est néanmoins configurable en fonction des besoins.
{note:title=Rappel}
Pour tester l'apparition du WaitingPanel dans les test-releases, deux cas de figures se présentent :
* Si l'action qui fait apparaitre le WaitingPanel ne provoque pas d'affichage de fenêtre au cours de son traitement, il convient d'utiliser la balise ```assertProgressDisplay``` qui teste de manière atomique l'apparition et la disparition du WaitingPanel.\\
Par exemple : \\
```
<click name="ButtonPanelGui.okButton"/>
<assertProgressDisplay name="waitingPanel"/>
```

* Si l'action qui fait apparaitre le WaitingPanel provoque l'apparition d'une autre fenêtre, il convient d'utiliser la balise ```assertVisible``` pour "encadrer" ladite fenêtre.\\
Par exemple :\\
```
<click name="ButtonPanelGui.okButton"/>
<assertVisible name="waitingPanel" expected="true"/>
<assertFrame title="Erreur"/>
<assertValue name="errorMessage" expected="Erreur 30 - blablabla."/>
<click label="OK"/>
<assertVisible name="waitingPanel" expected="false"/>
```

* Si l'action qui fait apparaitre le WaitingPanel referme ensuite la fenêtre une fois le traitement terminé, il convient d'utiliser plutôt la balise ```assertFrame``` pour que le test se déroule correctement sinon on peut se retrouver avec des problèmes de synchronisation.\\
Par exemple :\\
```
<click label="Valider le chantier"/>
<assertFrame title="Validation du chantier"/>
...
<click name="ValidationChantier.ButtonPanelGui.okButton"/>
<assertFrame title="Validation du chantier" closed="true"/>
```
{note}