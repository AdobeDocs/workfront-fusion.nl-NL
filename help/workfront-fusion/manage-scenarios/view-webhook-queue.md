---
title: k's wachtrij
description: Veel services bieden websites voor het direct verzenden van meldingen wanneer zich een bepaalde wijziging in de service voordoet. Instant triggers, ook wel webhooks genoemd, kunnen deze gebeurtenissen gebruiken om scenario's te starten. De gebeurtenissen gaan in de rij van de website terwijl zij op verwerking wachten, zoals wanneer het scenario reeds loopt. U kunt de wachtrij van de website weergeven.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# De wachtrij van een webhaak weergeven

Veel services bieden websites voor het direct verzenden van meldingen wanneer zich een bepaalde wijziging in de service voordoet. Instant triggers, ook wel webhooks genoemd, kunnen deze gebeurtenissen gebruiken om scenario&#39;s te starten. De gebeurtenissen gaan in de rij van de website terwijl zij op verwerking wachten, zoals wanneer het scenario reeds loopt. U kunt de wachtrij van de website weergeven.

Binnenkomende webhaakgegevens worden altijd opgeslagen in de wachtrij, ongeacht hoe u de optie Gegevens hebt ingesteld, is vertrouwelijk in het deelvenster met scenario-instellingen. Nadat de gegevens in een scenario worden verwerkt, wordt het permanent geschrapt van de rij.

Voor meer informatie over webhooks, zie [ Onmiddellijke trekkers (webhooks) ](/help/workfront-fusion/references/modules/webhooks-reference.md).

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Elk Adobe Workfront Workflow-pakket en elk Adobe Workfront Automation and Integration-pakket</p><p>Workfront Ultimate</p><p>Workfront Prime en Select packages, met extra aanschaf van Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licenties</td> 
   <td> <p>Standard</p><p>Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

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
