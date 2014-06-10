---
layout: post
title: agf-test - Execution de plusieurs gui-test dans une même session
tags: [codjo-test,framework-1-50]
---
Ajout de 2 paramètres à la balise <gui-test> :
* shouldStop : Si shouldStop = "true" (valeur par défaut), la session sera fermée à la fin du gui-test&nbsp;sinon elle restera ouverte
* shouldStart : Si shouldStart = "true" (valeur par défaut), une session sera ouverte au début du gui-test sinon on utilisera la dernière ouverte.

Exemple d'utilisation :
\\
```
<gui-test shouldStop = "false">
 <assertFrame title="Titre Frame"/>
 <assertValue name="myTextField" expected="valeur initiale"/>
 <setValue name="myTextField" value="valeur modifiée"/>
</gui-test>

<gui-test shouldStart = "false">
 <assertValue name="myTextField" expected="valeur modifiée"/>
</gui-test>
```