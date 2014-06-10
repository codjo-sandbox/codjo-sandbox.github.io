---
layout: post
title: agf-release-test - Evolution sur balise Click
tags: [framework-1-99,codjo-release-test]
---
Il est maintenant possible d'utiliser la balise ```click``` avec, à la fois, le nom du composant et le label.

Ex: Sur ```JOptionPane```
```
<click name="JOptionPane.button" label="OK"/>
<click name="JOptionPane.button" label="ANNULER"/>

<click name="anotherButton" label="ANNULER"/>
```

Cela permet par exemple de cliquer sur un bouton dont le label est identique à un autre bouton.