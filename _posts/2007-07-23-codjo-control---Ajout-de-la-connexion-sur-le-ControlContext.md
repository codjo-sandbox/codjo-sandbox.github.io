---
layout: post
title: agf-control - Ajout de la connexion sur le ControlContext
tags: [framework-1-6,codjo-control]
---
La ```Connection``` a été ajouté sur le ```ControlContext```

Exemple d'utilisation dans un ```Control``` : 

```java
public class MyControl extends AbstractControl {
    public void control(Object obj, Dictionary dico) throws ControlException {
        try {
            Statement statement = getContext().getConnection().createStatement();
            try {
                statement.execute(MY_QUERY);
            }
            finally{
                statement.close();
            }
        }
        catch (SQLException e) {
            throw new ControlException(getErrorCode(), e);
        }
    }
}

```
