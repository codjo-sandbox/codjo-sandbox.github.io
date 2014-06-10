---
layout: post
title: agf-referential - Déplacement de méthode de la classe ReferentialItemPanel vers la classe Field
tags: [framework-1-90,codjo-referential]
---
La méthode ```isAuditField``` de ```ReferentialItemPanel``` a été déplacée dans la classe ```Field```

```title=Méthode isAuditField
    public boolean isAuditField() {
        return "audit".equals(getName());
    }
```

De plus, le morceau de code suivant de la classe ```ReferentialItemPanel```

```title=old code
type.toLowerCase().contains("integer")
                     || type.toLowerCase().contains("double")
                     || "big-decimal".equals(type)
                     || type.toLowerCase().contains("float")
                     || type.toLowerCase().contains("long")
```

a été transformé en méthode dans la classe ```Field```

```title=Nouvelle méthode isNumberField
public boolean isNumberField() {
        String lowerType = type.toLowerCase();
        return lowerType.contains("integer")
               || type.toLowerCase().contains("double")
               || "big-decimal".equals(type)
               || type.toLowerCase().contains("float")
               || type.toLowerCase().contains("long");
    }
```