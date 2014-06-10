---
layout: post
title: agf-maven-common - Correction des chemins de répertoires
tags: [framework-1-28,codjo-maven-common]
---
Correction des chemins de répertoires concernant les separateurs dans les fichiers parsés par le plugin config :

Avant dans le test-release.properties contenant des variables a remplacer :
```
...
myProperty = ${project.basedir}
...
```

le fichier généré était incorrect car '\' est un caractère d'échappement :
```
...
myProperty = C\:/DEV/projects/roses/
...
```

maintenant c'est corrigé et le fichier généré ressemble à :
```
...
myProperty = C:/DEV/projects/roses/
...
```