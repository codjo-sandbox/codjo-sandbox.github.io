---
layout: post
title: agf-workflow - Mise à disposition du message agent à l'ordonnanceur
tags: [framework-1-114,codjo-workflow]
---
Les agents de type ```ScheduleAgent``` permettent de déclencher une tâche après une autre en appelant un objet composite de type ```ScheduleAgent.Handler```. Cette interface a été modifiée pour permettre de récupérer le ```AclMessage``` manipulé par le ```ScheduleLeader```.

Ce message contient notamment le ```UserId``` de l'utilisateur connecté, ce qui permet de créer des connexions à la base de données grâce au ```JdbcServiceHelper```.

<u>Exemple</u> : pour déclencher une segmentation après une tâche de type ```prodcom``` :
```
public class AfterProdcomAgent extends ScheduleAgent {
    public AfterProdcomAgent() {
        super(new AfterProdcomHandler());
    }

    private static class AfterProdcomHandler extends ScheduleAgent.AbstractHandler {
        public boolean acceptContract(ScheduleContract contract) {
            return "prodcom".equals(contract.getRequest().getType());
        }

        public JobRequest createNextRequest(ScheduleContract contract) {
            [[...]]
            try {
                ConectionPool pool = jdbcServiceHelper.getPool(getMessage().decodeUserId());
                Statement stm = pool.getConnection().createStatement();
                [[...]]
            } catch (Exception ex) {
            }
        }
    }
}
```