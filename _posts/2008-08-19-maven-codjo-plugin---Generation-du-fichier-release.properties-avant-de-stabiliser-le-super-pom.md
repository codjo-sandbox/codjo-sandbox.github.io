---
layout: post
title: maven-agf-plugin - Génération du fichier release.properties avant de stabiliser le super-pom
tags: [framework-1-57,maven-codjo-plugin]
---
Un nouveau goal ```release``` a été ajouté qui, en plus de mettre à jour les nouvelles versions des librairies ou plugins... passés en snapshot, génère un fichier ```release.properties``` contenant la nouvelle version du framework, le tag associé et la version de développement du framework.

Ce fichier est utilisé lors de l'exécution du goal ```release:prepare``` pour outrepasser les étapes de saisie des versions.

Exemple de contenu :
```
1.release configuration
project.dev.com.agf.pom\:codjo-pom-plugin=SNAPSHOT
project.rel.com.agf.pom\:codjo-pom-application=1.19
scm.tag=codjo-pom-1.19
scm.url=scm\:svn\:http://bd-subversion/codjo-pom/trunk
project.dev.com.agf.pom\:codjo-pom-application=SNAPSHOT
project.dev.com.agf.pom\:codjo-pom=SNAPSHOT
project.rel.com.agf.pom\:codjo-pom-plugin=1.19
project.dev.com.agf.pom\:codjo-pom-library=SNAPSHOT
project.rel.com.agf.pom\:codjo-pom-library=1.19
completedPhase=map-development-versions
project.rel.com.agf.pom\:codjo-pom=1.19

```