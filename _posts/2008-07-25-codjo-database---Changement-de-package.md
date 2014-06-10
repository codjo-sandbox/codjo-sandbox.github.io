---
layout: post
title: agf-database - Changement de package
tags: [framework-1-54,codjo-database]
---
Les différentes classes se trouvant à la racine de ```com.agf.database.common``` ont été copiées vers ```com.agf.database.common.api```.
Les anciennes classes ont été marquées ```@Deprecated```.
L'ancienne factory ```com.agf.database.common.DatabaseFactory``` a été modifiée afin de garantir une compatibilité ascendante.