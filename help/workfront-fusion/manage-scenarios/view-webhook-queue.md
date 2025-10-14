---
title: k's wachtrij
description: Veel services bieden websites voor het direct verzenden van meldingen wanneer zich een bepaalde wijziging in de service voordoet. Instant triggers, ook wel webhooks genoemd, kunnen deze gebeurtenissen gebruiken om scenario's te starten. De gebeurtenissen gaan in de rij van de website terwijl zij op verwerking wachten, zoals wanneer het scenario reeds loopt. U kunt de wachtrij van de website weergeven.
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# De wachtrij van een webhaak weergeven

Veel services bieden websites voor het direct verzenden van meldingen wanneer zich een bepaalde wijziging in de service voordoet. Instant triggers, ook wel webhooks genoemd, kunnen deze gebeurtenissen gebruiken om scenario&#39;s te starten. De gebeurtenissen gaan in de rij van de website terwijl zij op verwerking wachten, zoals wanneer het scenario reeds loopt. U kunt de wachtrij van de website weergeven.

Binnenkomende webhaakgegevens worden altijd opgeslagen in de wachtrij, ongeacht hoe u de optie Gegevens hebt ingesteld, is vertrouwelijk in het deelvenster met scenario-instellingen. Nadat de gegevens in een scenario worden verwerkt, wordt het permanent geschrapt van de rij.

Voor meer informatie over webhooks, zie [&#x200B; Onmiddellijke trekkers (webhooks) &#x200B;](/help/workfront-fusion/references/modules/webhooks-reference.md).

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licentie</td> 
   <td> <p>Nieuw: Standaard</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidig: Geen Workfront Fusion-licentievereisten.</p>
   <p>of</p>
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] Workfront-abonnement: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>[!UICONTROL Ultimate] Workfront-abonnement: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## De wachtrij van een webhaak weergeven

Alle berichten van binnenkomende webhooks worden opgeslagen in de wachtrij van de website.

Als een scenario momenteel een rij heeft, toont een banner in dat scenario:

![&#x200B; banner van de Rij &#x200B;](assets/queue-banner.png)

De wachtrij van een webhaak weergeven:

1. Klik op **[!UICONTROL Webhooks]** in het menu links.
1. Zoek de Webhaak waarvoor u de wachtrij wilt weergeven.
1. Zoek het aantal gebeurtenissen op de knop Ontvangen gebeurtenissen.

   ![&#x200B; de rij van Webhaak &#x200B;](assets/webhook-queue.png)

1. Klik op de knop om details over gebeurtenissen in de wachtrij weer te geven.
