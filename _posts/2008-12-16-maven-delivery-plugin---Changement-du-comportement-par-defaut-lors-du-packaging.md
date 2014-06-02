---
layout: post
title: maven-delivery-plugin - Changement du comportement par défaut lors du packaging
tags: [framework-1-76,maven-delivery-plugin]
---
Le comportement par défaut du plugin lors du packaging a été modifié. Maintenant le plugin prendra par défaut tous les fichiers se trouvant dans les répertoires ```src/script```, ```src/config```, ```src/binary``` (cf. [[/2008/12/17/maven-delivery-plugin - Modification des répertoires de packaging]]) . Un mécanisme d'exclusion a été ajouté afin de pouvoir affiner le packaging.

<u>Pour rappel</u> :
** **```src/script```** contient les scripts d'exécution (**.sh, \*.cmd, etc).
Ces fichiers seront filtrés  avant d'être ajouté au zip final. _Exemple_ : ```$\{artifactId```} devient ```myapp-gui```.
** **```src/config```* contient les fichiers de configuration. 
Ces fichiers seront filtrés et "templatisé" avant d'être ajouté au zip final. _Exemple_ : le fichier ```server-config.properties``` devient ```server-config.properties.template```, de plus les variables de livraison (ex. ```\@databaseUrl@```) ne sont pas remplacées
** **```src/binary```* contient tous les fichiers devant être considéré comme des fichiers binaires.

<u>Exemple</u> : Si on considère le projet suivant : 
{noformat}
myapp-batch/
  | pom.xml
  | src/
  |  | script/
  |  |   do-foo.cmd
  |  |   do-bar.cmd
{noformat}
Par défaut le zip final contiendra l'arborescence suivante :
{noformat}
BATCH/
  | do-foo.cmd
  | do-bar.cmd
  | *.jar
{noformat}
Si on veux que le fichier ```do-foo.cmd``` ne fasse pas partie du livrable final, il suffit de configurer ```maven-delivery-plugin``` dans le ```pom.xml``` de la façon suivante :
```xml
<plugin>
    <groupId>com.agf.maven.mojo</groupId>
    <artifactId>maven-delivery-plugin</artifactId>
    <configuration>
        <descriptorId>batch</descriptorId>
        <excludes>
            <exclude>
                <file>do-foo.cmd</file>
            </exclude>
        </excludes>
    </configuration>
</plugin>
```

