---
layout: post
title: agf-mad - Refactoring de RequestRecordNavigator
tags: [framework-1-91,codjo-mad]
---
La classe ```RequestRecordNavigator``` a été remaniée :
- Les listeners ```MouseListener``` et ```KeyListener``` sont créés dans le constructeur,
- Dans ```initialize(RequestTable)```, un listener est ajouté sur le ```DataSource``` plutôt que sur la ```RequestTable```.
