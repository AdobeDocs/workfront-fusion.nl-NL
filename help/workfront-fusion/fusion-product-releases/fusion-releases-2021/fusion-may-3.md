---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: 'Workfront Fusion release activity: Week van 3 mei 2021'
description: Op deze pagina worden alle verbeteringen beschreven die in Adobe Workfront Fusion in de week van 3 mei 2021 zijn aangebracht.
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 8858fc79-5eda-4938-9bb5-c05be38f02bc
source-git-commit: 0e8f73afb2ab60bb1b601abf3c4f3d611e97d125
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Workfront Fusion release activity: Week van 3 mei 2021

Op deze pagina worden alle verbeteringen beschreven die in Adobe Workfront Fusion in de week van 3 mei 2021 zijn aangebracht.

Voor een lijst van alle recente veranderingen, zie [ de versieactiviteit van de Fusie van Adobe Workfront ](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Voor een lijst van recente insectenmoeilijke situaties in de Fusie van Workfront, zie de [ pagina van de Updates van het Onderhoud van Workfront ](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html) en controleer om het even welke updates geëtiketteerd de Update van het Onderhoud van de Fusie van Workfront.

## Salesforce-connector kan nu zoeken met SOQL

De module Salesforce > Zoeken naar records heeft nu de optie om te zoeken met SOQL (Salesforce Object Query Language). U kunt ook zoeken met de eerder beschikbare opties (SOSL en eenvoudige zoekopdrachten).

## Voor een nieuw verbindingstype in de Azure DevOps-connector is minder bereik vereist

Om de beveiliging te verbeteren, hebben we een nieuw connectortype toegevoegd aan de Workfront Fusion Azure DevOps Connector. Wanneer u nu een verbinding maakt in een Azure DevOps-module, kunt u kiezen uit twee typen verbindingen:

* Azure DevOps

  Dit nieuwe verbindingstype beperkt werkingsgebieden tot die specifiek nodig door Workfront Fusion.

* Azure DevOps (alle bereik aanvragen)

  Dit is het verouderde verbindingstype, dat alle bereik opvraagt dat beschikbaar is in een verbinding met Azure DevOps.

We raden u aan het Azure DevOps-verbindingstype te gebruiken in al uw nieuwe scenario&#39;s die Azure DevOps gebruiken. Wij adviseren ook dat u om het even welke modules Azure DevOps in uw bestaande scenario&#39;s verandert om het nieuwe verbindingstype te gebruiken. Het oude verbindingstype Azure DevOps (Request all scope) wordt in de nabije toekomst vervangen.
