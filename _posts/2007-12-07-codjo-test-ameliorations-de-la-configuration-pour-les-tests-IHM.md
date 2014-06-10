---
layout: post
title: agf-test améliorations de la configuration pour les tests IHM
tags: [framework-1-23,codjo-test,hot-topics]
---
Les améliorations apportées sont les suivantes :
** Suppression de la propriété **gui.start.method* (implicitement, c'est la méthode 'main' qui est autorisée),
** Possibilité de remplacer les arguments **0, 1, 2, 3** par **user, password, server.host, server.port*,
** Remplacement des propriétés **gui.start.class** et **gui.start.arg.**{**}{_}argName{_}** par **gui.default.class** et **gui.default.arg.**{**}{_}argName{_}{*}_,_
** Ajout d'une propriété optionnelle **gui.default.arg.specific* pour ajouter des arguments optionnels,
* Pour les configurations spécifiques, il n'est plus nécessaire de redéfinir les propriétés redondantes. Chaque propriété hérite de la propriété 'default' associée,
* Suppression du code spécifique weblogic.

<table style='background-color: #FFCCCC;'>
       <colgroup><col width='24'><col></colgroup>
         <tr>
           <td valign='top'><img src='attachments/forbidden.gif' width='16' height='16' align='absmiddle' alt='' border='0'></td>
           <td><p>A la suite des modifications effectuées, **il est indispensable de modifier le fichier test-release.config pour que les tests IHMs continuent de passer**. Ainsi, si les paramètres de configuration sont définis ainsi :
```
gui.start.class = ${clientMainClass}
gui.start.method = main
gui.start.arg.0 = ${defaultTestUser}
gui.start.arg.1 = ${defaultTestUserPassword}
gui.start.arg.2 = ${serverHost}
gui.start.arg.3 = ${serverPort}
```
Il faut les modifier comme ceci :
```
gui.default.class = ${clientMainClass}
gui.default.arg.user = ${defaultTestUser}
gui.default.arg.password = ${defaultTestUserPassword}
gui.default.arg.server.host = ${serverHost}
gui.default.arg.server.port = ${serverPort}
```
ou comme cela :
```
gui.default.class = ${clientMainClass}
gui.default.arg.0= ${defaultTestUser}
gui.default.arg.1= ${defaultTestUserPassword}
gui.default.arg.2 = ${serverHost}
gui.default.arg.3 = ${serverPort}
```
</p></td>
          </tr>
</table>
\\
**Exemples de configuration possible :**
\\

Pour ajouter un argument spécifique dans la configuration par défaut :
\\
```
gui.default.class = ${clientMainClass}
gui.default.arg.user = ${defaultTestUser}
gui.default.arg.password = ${defaultTestUserPassword}
gui.default.arg.server.host = ${serverHost}
gui.default.arg.server.port = ${serverPort}
gui.default.arg.specific = argumentSpecifique
```
Pour créer une configuration spécifique nommée **'test'** identique à la configuration par défaut mais avec une autre classe de démarrage et un autre argument spécifique, il suffit en raison de l'héritage de redéfinir les propriétés gui.test.class et gui.test.arg.specific, par exemple :
\\
```
gui.test.class = ${clientTestClass}
gui.test.arg.specific = argumentSpecifiqueTest
```