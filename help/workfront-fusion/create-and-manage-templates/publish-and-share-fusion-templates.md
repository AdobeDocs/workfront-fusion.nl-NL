---
title: Publish en gedeelde sjablonen
description: Wanneer u een malplaatje creeert, wordt uw malplaatje beschikbaar voor al uw teamleden. Als u het malplaatje met iemand buiten uw team wilt delen, moet u het eerst publiceren.
author: Becky
feature: Workfront Fusion
exl-id: 99a1227d-bff9-479f-b8b9-efcf7cea3708
source-git-commit: 7acc27ab2ce80b964b7f9fbb302816aa75964ab5
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# Publish en gedeelde sjablonen

Wanneer u een malplaatje creeert, wordt uw malplaatje beschikbaar voor al uw teamleden. Als u het malplaatje met iemand buiten uw team wilt delen, moet u het eerst publiceren.

Voor informatie bij het creëren van een malplaatje, zie [ een nieuw malplaatje ](/help/workfront-fusion/create-and-manage-templates/create-new-fusion-templates.md) creëren.

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

## Vereisten

Er moet een sjabloon worden gemaakt voordat deze kan worden gepubliceerd of gedeeld.

## Publish een sjabloon

1. Klik in het navigatievenster aan de linkerkant op **[!UICONTROL Templates]** .
1. Klik op de tab **[!UICONTROL Team templates]** .
1. Klik **Publish** in de lijn van het malplaatje u wilt publiceren.

   of


   Klik op de naam van de sjabloon die u wilt publiceren en klik vervolgens op de knop **[!UICONTROL Publish]** in de rechterbovenhoek van het scherm.

## Een [!DNL Workfront Fusion] -sjabloon delen

Nadat u een sjabloon hebt gepubliceerd, kunt u deze delen.

1. Klik in het navigatievenster aan de linkerkant op **[!UICONTROL Templates]** .
1. Klik op de tab **[!UICONTROL Team templates]** .
1. Klik op de naam van de sjabloon die u wilt delen om de sjabloon te openen.
1. Klik op het **Gepubliceerde** lusje om die versie van het malplaatje te openen.
1. (Voorwaardelijk) Als u een deelbare koppeling wilt, klikt u op **[!UICONTROL Share public link]** .

   >[!NOTE]
   >
   >Hoewel u deze koppeling kunt delen, blijft de sjabloon zelf op het tabblad [!UICONTROL Team templates] staan en is deze niet openbaar.

1. (Voorwaardelijk) Als u wilt dat de sjabloon openbaar wordt, stuurt u de sjabloon naar de beheerder voor goedkeuring door op **[!UICONTROL Request Approval]** te klikken.

   >[!NOTE]
   >
   >* Nadat het malplaatje wordt goedgekeurd, wordt het openbaar. [!UICONTROL Public templates] zijn zichtbaar op het tabblad [!UICONTROL Public templates] voor alle [!DNL Workfront Fusion] -gebruikers, ongeacht de organisatie of het team.
   >* Uw beheerder wordt niet op de hoogte gesteld van het ontvangen van de sjabloon die per e-mail kan worden gecontroleerd. Als de goedkeuring dringend is, contacteer direct de beheerder.


## Sjabloonstatussen

Fusion slaat de verschillende versies (Privé, Gepubliceerd en Goedgekeurd) op verschillende tabbladen van de sjabloonpagina op.

De volgende statussen zijn beschikbaar:

* **[!UICONTROL Private]**: Deze sjabloon is alleen zichtbaar voor de sjabloonauteur en zijn team.
* **[!UICONTROL Published]**: Deze sjabloon is alleen zichtbaar voor de sjabloonauteur en zijn team. U kunt gepubliceerde sjablonen ter goedkeuring verzenden en een deelbare koppeling kopiëren.
* **[!UICONTROL Approved]**: Deze sjabloon is zichtbaar voor alle Workfront Fusion-gebruikers op het tabblad [!UICONTROL Public templates] . U kunt een deelbare koppeling kopiëren door op [!UICONTROL Options] in de rechterbovenhoek van het scherm te klikken.

<!--You can also check the status from the [!UICONTROL Team templates] tab. If a template is published, it will have an icon to the right of the template name.

* **Eye icon**: The template is published, it is visible only for the team, and the approval request was not sent.
* **Yellow checkmark icon**: The template is published, it is visible only for the team, and the approval request was sent.
* **Green checkmark icon**: The template is published and public. It is visible for any Workfront Fusion user in the [!UICONTROL Public templates] tab. It is also still visible in the [!UICONTROL Team templates] tab, and the template author or their team member can still edit it.

Templates without icons have [!UICONTROL Private] status. They are not published and are visible only to the team.
-->
