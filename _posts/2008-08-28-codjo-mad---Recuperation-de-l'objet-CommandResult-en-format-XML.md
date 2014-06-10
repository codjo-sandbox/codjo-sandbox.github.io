---
layout: post
title: agf-mad - Récupération de l'objet CommandResult en format XML
tags: [framework-1-59,codjo-mad]
---
Ajout dans la classe ```CommandResult``` d'une fonction ```toXML``` permettant de récupérer cette classe sous format XML.
```
 public String toXML() {

       StringBuffer buffer = new StringBuffer();
       if (result instanceof ResultTable) {
                return buffer.append(((ResultTable)result).toXML()).toString();
        }
        return buffer.append("<row><field name=\"").append(fieldName).append("\"><![CDATA[")
              .append(result).append("]]></field></row>")
               .toString();
 }
```
&nbsp;A titre d'exemple, cette fonction est utilisée, via la fonction ```proceed``` par la classe HandlerCommand&nbsp; afin d'envoyer le résultat de son exécution à son client
```
     public String proceed(Node node) throws HandlerException {
        try {
            CommandResult commandResult = executeQuery(new CommandQuery(node));

            StringBuffer result = buildResponseHeader(node);
            result.append(commandResult.toXML());
            result.append("</result>");
            return result.toString();
        }
        catch (HandlerException ex) {
            throw ex;
        }
        catch (Exception ex) {
            throw new HandlerException(ex);
        }
    }
 
```
De plus, cette fonction permet aussi de tester le résultat d'un ```HandlerCommand``` dans un test unitaire.

**Exemple :**
```
     public void test_calculs() throws Exception {
        fixture.insertInputInDb("GetFofInformationsForViewsHandlerTest.tokio");
        HandlerCommand.CommandResult result = assertExecuteQuery(
              "GetFofInformationsForViewsHandlerTest.tokio",
              buildArgument());

        String expected = "<row>"
                          + "<field name=\"pl\"><![[CDATA[null]]]></field>"
                          + "<field name=\"cash\"><![[CDATA[]]]></field>"
                          + "<field name=\"currentPercentHedged\">63.69</field>"
                          + "<field name=\"currentHedged\">-32000000.00</field>"
                          + "<field name=\"currentHolding\">50244153.22</field>"
                          + "<field name=\"ptfAverPrice\"><![[CDATA[null]]]></field>"
                          + "<field name=\"monthlyAverHedging\">-2666666.67</field>"
                          + "</row>";
        assertEquals(expected, result.toXML());
    }
```