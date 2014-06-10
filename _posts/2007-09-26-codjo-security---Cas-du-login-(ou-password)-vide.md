---
layout: post
title: agf-security - Cas du login (ou password) vide
tags: [codjo-security,framework-1-13]
---
Les cas de login et de mot de passe vide sont maintenant correctement rejeté par la couche de sécurité. Précédemment l'authentification _Active Directory_ ne signalait pas l'erreur.