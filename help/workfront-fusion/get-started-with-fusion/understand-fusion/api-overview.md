---
title: API-overzicht
description: API's (Application Programming Interfaces) zijn een manier waarop toepassingen en services met elkaar kunnen communiceren. Fusion gebruikt API's om te communiceren met de toepassing waarmee u verbinding maakt. Elke toepassing heeft een aparte API.
author: Becky
feature: Workfront Fusion
source-git-commit: f5dcb5207581fb68d0f3048d23214d08a28f2f22
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Overzicht van API&#39;s in Fusion

<!--Add me to TOCs-->

API&#39;s (Application Programming Interfaces) zijn een manier waarop toepassingen en services met elkaar kunnen communiceren. Fusion gebruikt API&#39;s om te communiceren met de toepassingen waarmee u verbinding maakt.

API&#39;s worden gemaakt en beheerd door de eigenaars van de toepassing. De Workfront API is bijvoorbeeld eigendom van het Workfront-team in Adobe en de Microsoft Graph API is eigendom van Microsoft. De eigenaar van de API bepaalt welke acties beschikbaar zijn via de API.

## Overwegingen

Het feit dat API&#39;s door hun eigenaars en niet door Fusion worden gedefinieerd, leidt tot enkele belangrijke overwegingen:

* **u kunt Fusion gebruiken om met om het even welke app of dienst te verbinden die openbare API** heeft, al dan niet biedt de Fusie een specifieke schakelaar aan die app of de dienst aan. U kunt de universele connectors van Fusion gebruiken om deze apps of services in uw scenario&#39;s te brengen.

  Voor een lijst van universele schakelaars, zie [&#x200B; Universele schakelaars &#x200B;](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)

* **de Veranderingen die in API van een toepassing door zijn eigenaar worden aangebracht kunnen de functionaliteit van de Fusie beïnvloeden.** Als de wijzigingen ernstig genoeg zijn, moet Fusion mogelijk modules of verbindingstypen bijwerken of in extreme gevallen een nieuwe connector voor de toepassing maken.

  Voor meer informatie over deze extreme situaties, die als &quot;het breken veranderingen worden bekend,&quot;zie [&#x200B; het breken veranderingen &#x200B;](#breaking-changes) in dit artikel.


## Wijzigingen verbreken

Een algemene oorzaak voor het doorbreken van wijzigingen is afleiding, wanneer een eigenaar van een API een API geheel of gedeeltelijk uit de beschikbaarheid verwijdert. Wanneer dit gebeurt, doet het Fusion-team al het mogelijke om de Fusion-functionaliteit snel opnieuw uit te lijnen met de nieuwe versie van de API van de toepassing. Dit neemt gewoonlijk de vorm van nieuwe modules, verbindingstypes, of schakelaars.

Omdat uw scenario&#39;s van de Fusie met uw specifieke gegevens worden gevormd, kunt u uw scenario&#39;s moeten bijwerken.

* Als de wijzigingen betrekking hadden op verificatie of verificatie, moet u mogelijk de verbindingen voor die toepassing bijwerken.
* Als de veranderingen met een specifieke actie (eindpunt) in API verwant waren, kunt u om het even welke module met betrekking tot die actie aan een nieuwe versie van de module moeten bijwerken.
* Als de volledige API versie die door Fusion wordt gebruikt verouderd is, kunt u alle modules van die schakelaar aan een nieuwe versie van de schakelaar moeten bijwerken.

In veel gevallen, kunt u aan de nieuwe versie van een module bevorderen zonder het moeten die module aanpassen.

Voor informatie en instructies bij de bevordering van een module, zie [&#x200B; Verbetering een module aan een nieuwe versie &#x200B;](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md).
