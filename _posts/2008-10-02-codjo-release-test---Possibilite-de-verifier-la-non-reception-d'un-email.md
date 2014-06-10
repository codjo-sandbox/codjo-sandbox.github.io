---
layout: post
title: agf-release-test - Possibilité de vérifier la non réception d'un email
tags: [framework-1-64,codjo-release-test]
---
La balise ```<message>``` contenue dans la tâche ```<assert-inbox>``` peut maintenant prendre un argument ```present``` qui indique si l'email est attendu ou non.
* true : Vérifie que le message est reçu (valeur par défaut).
* false : Vérifie que le message n'est pas reçu.

Exemple :
```
<start-mail-server .../>
...
<assert-inbox>
   <message from="luke@rebels.org" to="dark@vador.net" subject="Réconciliation" present="false"/>
</assert-inbox>
```
Doc : [[codjo-release-test - Tags email#message]]