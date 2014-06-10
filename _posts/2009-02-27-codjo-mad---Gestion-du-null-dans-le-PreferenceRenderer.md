---
layout: post
title: agf-mad - Gestion du null dans le PreferenceRenderer
tags: [codjo-mad,framework-1-85]
---
La méthode suivante ne gérait pas le paramètre value à null.
```public Component getTableCellRendererComponent(JTable table, Object value, boolean isSelected, boolean hasFocus, int row, int column)```

Il a été géré comme la chaîne "null".