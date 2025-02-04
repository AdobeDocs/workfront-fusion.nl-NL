---
title: De Scenario-score-expert uitvoeren
description: De het Scoren Deskundige van het Scenario kan u helpen ervoor zorgen dat uw scenario op een manier wordt gevormd die beste praktijken volgt. Het controleert uw scenario en geeft aanbevelingen voor zijn structuur en organisatie.
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
source-git-commit: 1ac1c4358901ef81bb7375c24fcdf1a44119af13
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# De Scenario-score-expert uitvoeren

>[!IMPORTANT]
>
>De Scenario-score-expert is tijdelijk uitgeschakeld.

De het Scoren Deskundige van het Scenario kan u helpen ervoor zorgen dat uw scenario op een manier wordt gevormd die beste praktijken volgt. Het controleert uw scenario en geeft aanbevelingen voor zijn structuur en organisatie.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] package</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie</td> 
   <td> <p>Nieuw: [!UICONTROL Standard]</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidig: Geen [!DNL Workfront Fusion] vereiste licentie.</p>
   <p>of</p>
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] [!DNL Workfront] -abonnement: uw organisatie moet het abonnement aanschaffen [!DNL Adobe Workfront Fusion] .</li><li>[!UICONTROL Ultimate] [!DNL Workfront] abonnement: [!DNL Workfront Fusion] is opgenomen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet [!DNL Adobe Workfront Fusion] aanschaffen.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configuraties op toegangsniveau*</td> 
   <td> 
     <p>U moet een [!DNL Workfront Fusion] beheerder voor uw organisatie zijn.</p>
     <p>U moet een [!DNL Workfront Fusion] beheerder voor uw team zijn.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## De Scenario-score-expert uitvoeren

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u de Deskundige van het Scorebord van het Scenario wilt in werking stellen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik het Scorende Deskundige pictogram van het Scenario van het Scorebord van het pictogram ![ Scenario die deskundige ](assets/scoring-expert-icon.png) dichtbij de bodem van het scherm.

   Het deelvenster Scenario Scoring Expert wordt geopend.
1. Klik **evalueren**.

De Scenario Scoring Expert keert een score van 10 terug, en toont welke controles zijn overgegaan of ontbroken. Als een controle heeft ontbroken, geeft de Scorende Deskundige van het Scenario aanbevelingen voor hoe te om ervoor te zorgen dat het scenario aan deze controles voldoet.

![ score Scenario ](assets/scenario-score.png)

## Scenario-scènecontroles

De Scenario Scoring Expert gebruikt de volgende controles:

* Het scenario moet worden genoemd.
* Alle modules moeten geëtiketteerd zijn.
* Het scenario moet op een geplaatst programma lopen.

  Voor instructies, zie [ Plan een scenario ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
* De grootte van de scenario blauwdruk moet onder 5 MB zijn.

  Voor meer informatie, zie [ de prestatiesgidsen van de Fusie ](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#scenarios).
* Als een Workfront-instant trigger wordt gebruikt, moet deze worden gefilterd.

  Voor instructies, zie [ de filters van het het abonnementsabonnement van de Gebeurtenis in  [!DNL Workfront] > [!UICONTROL Watch Events] module ](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules).
