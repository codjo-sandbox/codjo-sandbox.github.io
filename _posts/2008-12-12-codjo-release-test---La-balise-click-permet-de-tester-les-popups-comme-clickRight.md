---
layout: post
title: agf-release-test - La balise click permet de tester les popups comme clickRight
tags: [framework-1-75,codjo-release-test]
---
La balise ```click``` s'enrichit pour pouvoir tester l'ouverture de popups de la même façon que la balise ```clickRight```.

**{<u>}Exemple :</u>**
```
<click name="MyButton">
  <assertEnabled menu="Lancer le calcul" expected="true"/>
  <select label="Lancer le calcul"/>
</click>
```