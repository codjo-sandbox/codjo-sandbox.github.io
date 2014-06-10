---
layout: post
title: agf-test - Ajout assert d'images de composants
tags: [framework-1-42,codjo-test]
---
Pour tester les graphes sous JFreeChart : création d'une nouvelle balise de step :

<assertComponentImage name="myJFreeChartPanel" expected="MyJFreeChartPanel_etalon.jpg"/>

Le test va générer un fichier jpg temporaire à partir du JComponent désigné par le champ "name" et le comparer à l'aide d'un checksum au fichier étalon désigné par le champ "expected".

Si les images ne sont pas identiques le test échoue. Attention : ce test est sensible à toute modification d'UI : évitez de tester un component basé sur un look and feel.