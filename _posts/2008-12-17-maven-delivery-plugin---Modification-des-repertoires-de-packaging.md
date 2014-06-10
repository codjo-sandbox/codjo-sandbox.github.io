---
layout: post
title: maven-delivery-plugin - Modification des répertoires de packaging
tags: [framework-1-76,maven-delivery-plugin]
---
* Le répertoire ```src/bin``` a été renommé en ```src/script```.
* Un nouveau répertoire ```src/binary``` est pris en compte lors de la création du livrable. Ce répertoire a pour vocation de contenir tous les fichiers binaires devant être inclus dans le livrable. Par défaut tous les fichiers contenus dans ce répertoire se trouveront dans le livrable final.

<u>Exemple</u> Pour ajouter une image ```my-icon.png``` à un livrable client. Il suffit d'avoir l'arborescence suivante:
{noformat}
myapp-gui/
  | pom.xml
  | src/
  |  | binary/
  |  |   my-icon.png
{noformat}
Le zip final sera de la forme
{noformat}
CLIENT/
  | my-icon.png
  | myapp-gui.jnlp.template
  | *.jar
{noformat}