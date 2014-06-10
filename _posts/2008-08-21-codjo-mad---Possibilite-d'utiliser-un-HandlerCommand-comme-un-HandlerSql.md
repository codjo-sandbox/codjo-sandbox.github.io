---
layout: post
title: agf-mad - Possibilité d'utiliser un HandlerCommand comme un HandlerSql
tags: [framework-1-56,codjo-mad]
---
Lors de la réception d'une requête, le handler manager prendra en compte les arguments passés dans un "selector" si "args" n'existe pas.

**existant (prioritaire):**
```
<?xml version="1.0"?>
<requests>
	..
	<command request_id="10">
		<id>handlerName</id>
		<args>
			<field name="name" value="value"/>
		</args>
	</command>
</requests>
```

**nouveau :**
```
<?xml version="1.0"?>
<requests>
	..
	<select request_id="3">
		<id>hanlderName</id>
		<selector>
			<field name="name" value="value"/>
			...
		</selector>
		<attributes>
			...
		</attributes>
		<page num="1" rows="1000"/>
	</select>
</requests>
```

Cela permet entre autre d'utiliser le ```HandlerCommand``` avec une ```RequestTable``` en définissant le handler dans le fichier "preference.xml".