---
layout: post
title: agf-pom - Ajout de la librairie Mockito
tags: [framework-1-41,hot-topics,codjo-pom]
---
La librairie Mockito a été ajoutée au super-pom. C'est une librairie de mock très simple à utiliser. Pour l'utiliser dans vos tests, ajouter ceci dans votre fichier pom.xml : 
```
<dependency>
   <groupId>org.mockito</groupId>
   <artifactId>mockito</artifactId>
   <scope>test</scope>
</dependency>
```

Exemples d'utilisation :

Stubbing (surcharge d'une valeur de retour d'une méthode) :
```
//You can mock concrete classes, not only interfaces
LinkedList mockedList = Mockito.mock(LinkedList.class);
 
//stubbing - before execution
Mockito.stub(mockedList.get(0)).toReturn("first");
 
assertEquals("first", mockedList.get(0));
assertNull(mockedList.get(999));
```

Verification des appels de méthode :
```
//mock creation
List mockedList = Mockito.mock(List.class);
 
//using mock object - will never throw any unexpected exception!
mockedList.add("one");
mockedList.clear();
 
//verification - if fails then it will throw an assertion error here:
Mockito.verify(mockedList).add("one");
Mockito.verify(mockedList).clear();
```

cf : http://code.google.com/p/mockito/