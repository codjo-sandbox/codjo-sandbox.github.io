---
layout: post
title: agf-pom - Modification du cycle de vie des tests release
tags: [codjo-pom,framework-1-26]
---
Le cycle de vie des tests release a été légèrement modifié, afin de permettre d'avoir des tests release écrit en java.

<u>Avant</u>
{noformat} 
phase   : pre-integration-test
execute :   
  deliver-batch
  stop-web
  stop-server
  deliver-server
  start-server
  deliver-web
  start-web
{noformat} 

<u>Maintenant</u>
{noformat} 
phase   : generate-test-sources
execute :   
  deliver-batch
  stop-web
  stop-server
  deliver-server
  deliver-web

phase   : pre-integration-test
execute :   
  start-server
  start-web
{noformat} 
