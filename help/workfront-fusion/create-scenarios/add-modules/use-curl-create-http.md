---
title: Gebruik cURL om een HTTP-module toe te voegen
description: U kunt een cURL-aanvraag in uw scenario plakken en Fusion maakt een HTTP-module die is geconfigureerd via de cURL-aanvraag.
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
source-git-commit: 55fe4bc46bc50ad9ccfd1b234e89028cf3cd12d5
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Gebruik cURL om een HTTP-module toe te voegen

U kunt een cURL-aanvraag in uw scenario plakken en Fusion maakt een HTTP-module die is geconfigureerd via de cURL-aanvraag.

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
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Een HTTP-module maken van een cURL-aanvraag


Een HTTP-module maken met cURL:

1. Maak de tekst van het cURL-verzoek buiten Fusion, bijvoorbeeld in een teksteditor.
1. Kopieer de cURL-aanvraag naar het klembord.
1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u de module wilt tot stand brengen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik op om het even welke witte ruimte in de scenarioredacteur met de rechtermuisknop aan en selecteer **Deeg**.

   of

   Druk op Ctrl + V (Windows) of Cmd + V (Mac).


   Er wordt een HTML-module gemaakt.
1. Sleep de module om het met uw scenario te verbinden.

## Problemen oplossen

Als uw cURL niet in uw scenario kleeft, controleer uw browser montages om ervoor te zorgen dat het kleven van het klembord wordt toegelaten.
