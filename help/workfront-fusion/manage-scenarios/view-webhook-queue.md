---
title: k's wachtrij
description: Veel services bieden websites voor het direct verzenden van meldingen wanneer zich een bepaalde wijziging in de service voordoet. Instant triggers, ook wel webhooks genoemd, kunnen deze gebeurtenissen gebruiken om scenario's te starten. De gebeurtenissen gaan in de rij van de website terwijl zij op verwerking wachten, zoals wanneer het scenario reeds loopt. U kunt de wachtrij van de website weergeven.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: 3d06958b6f706f4f974230853fb6553232656fd3
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# De wachtrij van een webhaak weergeven

Veel services bieden websites voor het direct verzenden van meldingen wanneer zich een bepaalde wijziging in de service voordoet. Instant triggers, ook wel webhooks genoemd, kunnen deze gebeurtenissen gebruiken om scenario&#39;s te starten. De gebeurtenissen gaan in de rij van de website terwijl zij op verwerking wachten, zoals wanneer het scenario reeds loopt. U kunt de wachtrij van de website weergeven.

Binnenkomende webhaakgegevens worden altijd opgeslagen in de wachtrij, ongeacht hoe u de optie Gegevens hebt ingesteld, is vertrouwelijk in het deelvenster met scenario-instellingen. Nadat de gegevens in een scenario worden verwerkt, wordt het permanent geschrapt van de rij.

Voor meer informatie over webhooks, zie [ Onmiddellijke trekkers (webhooks) ](/help/workfront-fusion/references/modules/webhooks-reference.md).

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

## De wachtrij van een webhaak weergeven

Alle berichten van binnenkomende webhooks worden opgeslagen in de wachtrij van de website.

Als een scenario momenteel een rij heeft, toont een banner in dat scenario:

![ banner van de Rij ](assets/queue-banner.png)

De wachtrij van een webhaak weergeven:

1. Klik op **[!UICONTROL Webhooks]** in het menu links.
1. Zoek de Webhaak waarvoor u de wachtrij wilt weergeven.
1. Zoek het aantal gebeurtenissen op de knop Ontvangen gebeurtenissen.

   ![ de rij van Webhaak ](assets/webhook-queue.png)

1. Klik op de knop om details over gebeurtenissen in de wachtrij weer te geven.
