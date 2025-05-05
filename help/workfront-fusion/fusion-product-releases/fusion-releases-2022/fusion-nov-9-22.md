---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Workfront Fusion release activity: Week 7 november 2022'
description: Deze pagina beschrijft alle verbeteringen die in Adobe Workfront Fusion in de week van 7 november 2022 zijn aangebracht.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 9d58abd0-1fe7-43c8-a1ea-2fadea738590
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Workfront Fusion release activity: Week 7 november 2022

**de rijoptimalisering van de 0&rbrace; Webhaak**

De wachtrij van Fusion voor webhaken is geoptimaliseerd met deze release. De service die webhooks accepteert, staat nu los van wachtrijen en andere processen. Door deze wijziging kan Fusion webhaakwachtrijen sneller en consistenter verwerken.

Tijdens de implementatie van deze verandering, konden wij verwachte logboekverwerkingstijd beter voor een rij gevormde webhaakgebeurtenissen begrijpen. De webhaakviewerpagina van Fusion is naar verwachting niet ouder dan 1 minuut.

Navigeer naar Webhooks in linkernavigatie om webhaakgebeurtenissen in de wachtrij weer te geven. De pictogrammen van de vrachtwagen met een aantal in de teller wijzen op rijgebeurtenissen voor die webhaak. Klik op het vrachtwagenpictogram om de gebeurtenissen in de wachtrij te zien.


**Ongebruikte webhooks zal nu worden gedeactiveerd of worden geschrapt**

We hebben een aantal wijzigingen aangebracht in de manier waarop Workfront Fusion ongebruikte webhaken verwerkt. Webhooks worden nu automatisch gedeactiveerd als een van de volgende twee van toepassing is:

* De webhaak is langer dan vijf dagen niet verbonden met een scenario.
* De webhaak wordt alleen gebruikt in inactieve scenario&#39;s, die al meer dan 30 dagen inactief zijn.

gedeactiveerde webhaken worden automatisch verwijderd en niet geregistreerd als ze niet zijn aangesloten op scenario&#39;s en meer dan 30 dagen in de gedeactiveerde status zijn geweest.
