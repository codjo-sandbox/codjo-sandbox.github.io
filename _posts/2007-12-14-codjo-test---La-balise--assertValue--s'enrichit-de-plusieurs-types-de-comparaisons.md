---
layout: post
title: agf-test - La balise "assertValue" s'enrichit de plusieurs types de comparaisons
tags: [codjo-test,framework-1-24]
---
La balise **assertValue** était limitée à effectuer des comparaisons exactes au niveau des chaînes de caractères. A présent un attribut **matching** permet d'effectuer des comparaisons de type **contains**, **startsWith** ou **endsWith**. Le comportement actuel est assuré par un matching de type **equals**.

Par exemple, en considérant un composant ```myField``` de type ```JTextField``` contenant la valeur "Je suis ton père", les assertions suivantes s'avèrent exactes :

<u>Exemples</u>
```
<assertValue name="myField" expected="Je suis ton père"/>
<assertValue name="myField" expected="Je suis ton père" matching="equals"/>
<assertValue name="myField" expected="ton" matching="contains"/>
<assertValue name="myField" expected="Je suis" matching="startsWith"/>
<assertValue name="myField" expected="ton père" matching="endsWith"/>
```
