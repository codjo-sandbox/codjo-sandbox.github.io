---
layout: post
title: agf-mad - Contrôle de la compatibilté du client avec le serveur
tags: [framework-1-6,codjo-mad]
---
Dorénavant, un contrôle de la compatibilité du client et du batch avec le serveur est mis en place de façon automatique.

Concrétement, dans la classe ```InstituteAmbassadorParticipant```, on va vérifier que le numéro de version du client packagé dans le fichier MANIFEST.MF du jar du client applicatif (gui ou batch) est bien compatible avec celui présent dans le fichier du jar du serveur.
La règle est la suivante :
* si la version du serveur est nulle (i.e : version de dév), tous les clients sont acceptés
* si la version du serveur est renseigné, la version du client doit être superieure ou égale à celle-ci. Sinon, le message d'erreur suivant est affiché :
{quote}
**Version client incompatible avec le serveur.**
**Vous devez utiliser un client ayant une version égale ou supérieure à celle du serveur.**
**Version serveur : '1.01.00.00-a'**
**Version client : '1.00.00.00-a'**
**Merci de bien vouloir contacter ASSET-SVP pour mettre à jour votre client**
{quote}

NB : le serveur ne tombe plus si le client n'est pas compatible.