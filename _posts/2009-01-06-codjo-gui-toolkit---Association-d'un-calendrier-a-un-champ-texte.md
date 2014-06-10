---
layout: post
title: agf-gui-toolkit - Association d'un calendrier à un champ texte
tags: [framework-1-78,codjo-gui-toolkit]
---
Il est possible via le ```CalendarHelper``` d'ajouter un ```Calendar``` à un champ texte.
il est nécessaire de spécifier le format de date utilisé par le calendrier.

_exemple :_
```
calendarButton.addActionListener(new ActionListener(){
            public void actionPerformed(ActionEvent event) {
                CalendarHelper calendar = new CalendarHelper();
                calendar.askDialog(textField, calendarButton, "yyyy-MM-dd");
            }
        });
```