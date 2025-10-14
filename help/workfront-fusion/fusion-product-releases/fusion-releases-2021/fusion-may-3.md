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
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Workfront Fusion release activity: Week van 3 mei 2021

Op deze pagina worden alle verbeteringen beschreven die in Adobe Workfront Fusion in de week van 3 mei 2021 zijn aangebracht.

Voor een lijst van alle recente veranderingen, zie [&#x200B; de versieactiviteit van de Fusie van Adobe Workfront &#x200B;](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

Voor een lijst van recente insectenmoeilijke situaties in de Fusie van Workfront, zie de [&#x200B; pagina van de Updates van het Onderhoud van Workfront &#x200B;](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=nl-NL) en controleer om het even welke updates geëtiketteerd de Update van het Onderhoud van de Fusie van Workfront.

## Salesforce-connector kan nu zoeken met SOQL

De module Salesforce > Zoeken naar records heeft nu de optie om te zoeken met SOQL (Salesforce Object Query Language). U kunt ook zoeken met de eerder beschikbare opties (SOSL en eenvoudige zoekopdrachten).

## Voor een nieuw verbindingstype in de Azure DevOps-connector is minder bereik vereist

Om de beveiliging te verbeteren, hebben we een nieuw connectortype toegevoegd aan de Workfront Fusion Azure DevOps Connector. Nu, wanneer u een verbinding in een module van Azure DevOps creeert, kunt u uit twee soorten verbindingen selecteren:

* Azure DevOps

  Dit nieuwe verbindingstype beperkt werkingsgebieden tot die specifiek nodig door Workfront Fusion.

* Azure DevOps (alle bereik aanvragen)

  Dit is het verouderde verbindingstype, dat om alle werkingsgebied verzoekt beschikbaar in een verbinding aan Azure DevOps.

Wij adviseren dat u het Azure DevOps verbindingstype in al uw nieuwe scenario&#39;s gebruikt die Azure DevOps gebruiken. Wij adviseren ook dat u om het even welke Azure modules DevOps in uw bestaande scenario&#39;s verandert om het nieuwe verbindingstype te gebruiken. Het oudere Azure DevOps-verbindingstype (Request all scopes) wordt in de nabije toekomst vervangen.
