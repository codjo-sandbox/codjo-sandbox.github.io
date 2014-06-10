---
layout: post
title: agf-mad - Résultat matriciel pour un HandlerCommand
tags: [codjo-mad,framework-1-51]
---
Ajout de la possibilité de retourner plusieurs lignes pour un handler command qui précédemment ne permettait de renvoyer qu'un seul champ de résultat.

Création de la classe ```ResultTable``` qui permet de passer un résultat de requête avec plusieurs champs et plusieurs lignes.

Exemple d'utilisation:

```
public class MonHandlerCommand extends HandlerCommand {

public CommandResult executeQuery(CommandQuery query) throws SQLException {
[[..]]
    ResultSet resultSet = con.createStatement().executeQuery(selectQuery);
        ResultTable result = new ResultTable();

        List<String> pK = new ArrayList();
        pK.add("clé primaire");
        result.setPrimaryKey(pK);
        while (resultSet.next()) {
            result.addRow();


            result.addField("champ1", value1);
            result.addField("champ2", value2);
            result.addField("champ3", value3);
[[..]]
    return createResult(result);
```