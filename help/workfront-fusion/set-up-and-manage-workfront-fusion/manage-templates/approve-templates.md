---
content-type: reference
title: Sjablonen goedkeuren of afwijzen
description: In dit artikel wordt beschreven hoe u Fusion-sjablonen kunt goedkeuren of afwijzen.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: dafecd8b-96e5-46da-9ab6-15f0bc9b52a4
source-git-commit: 23e9f383b25c7b3789c413e557b94418e48a636b
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Sjablonen voor het tabblad Openbaar goedkeuren of afwijzen

Adobe Workfront Fusion-sjablonen zijn vooraf ontwikkelde scenario&#39;s die zijn ontworpen om verschillende workflows te automatiseren en te stroomlijnen. Met deze sjablonen kunnen gebruikers snel integratie en automatisering instellen zonder dat ze alles helemaal zelf hoeven te bouwen.

Als u een beheerder bent, kunt u kiezen al dan niet bepaalde malplaatjes met de volledige organisatie op het Openbare malplaatjes tabel zouden moeten worden gedeeld.

Gebruikers kunnen sjablonen verzenden die zij maken voor goedkeuring en die worden gedeeld op de pagina Openbare sjablonen. <!--do the have to be requested or can an admin just choose to approve?-->

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] plan</td>
      <td><p>Alle</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">[!DNL Adobe Workfront] licentie</td>
      <td><p>Nieuw: [!UICONTROL Standard]</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td>
      <td>
        <p>Huidig: Geen [!DNL Workfront Fusion] vereiste licentie.</p>
        <p>of</p>
        <p>Verouderd: alle</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Product</td>
      <td>
        <p>Nieuw:</p>
        <ul>
          <li>[!UICONTROL Select] of [!UICONTROL Prime] [!DNL Workfront] Plan: Uw organisatie moet het abonnement aanschaffen [!DNL Adobe Workfront Fusion] .</li>
          <li>[!UICONTROL Ultimate] [!DNL Workfront] Overzicht: [!DNL Workfront Fusion] is opgenomen.</li>
        </ul>
        <p>of</p>
        <p>Huidig: Uw organisatie moet [!DNL Adobe Workfront Fusion] aanschaffen.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on [!DNL Adobe Workfront Fusion] licenses, see [[!DNL Adobe Workfront Fusion] licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->

+++

## [!DNL Workfront Fusion] -sjablonen goedkeuren of afwijzen

Als u een sjabloon goedkeurt, wordt deze zichtbaar op het tabblad [!UICONTROL Public templates] en beschikbaar voor alle gebruikers.

Als u een sjabloon verwijdert, wordt deze verwijderd van het tabblad [!UICONTROL Public templates] en wordt deze alleen beschikbaar gesteld aan het team dat de sjabloon heeft gemaakt.

1. Klik op **[!UICONTROL Administration]** in het navigatievenster aan de linkerkant om het [!UICONTROL Administration] -gebied te openen.
1. Klik op **[!UICONTROL Templates]** in het navigatievenster aan de linkerkant.
1. Als u een sjabloon wilt goedkeuren, klikt u op **[!UICONTROL Approve]** rechts van de sjabloon.
1. Als u een sjabloon wilt afwijzen, klikt u op **[!UICONTROL Disapprove]** rechts van de sjabloon.

>[!NOTE]
>
>Als u de sjabloon goedkeurt die eerder is goedgekeurd en vervolgens is bewerkt, wordt de oorspronkelijke sjabloon overschreven door uw tweede goedkeuring.


## Sjabloonstatussen

U kunt de status op de sjabloonpagina onder de sjabloonnaam controleren.

De volgende statussen zijn beschikbaar:

* **[!UICONTROL Private]**: Deze sjabloon is alleen zichtbaar voor de sjabloonauteur en zijn team.
* **[!UICONTROL Published]**: Deze sjabloon is alleen zichtbaar voor de sjabloonauteur en zijn team. Na publicatie kunt u de sjabloon desgewenst ter goedkeuring verzenden. U kunt ook een deelbare koppeling kopiëren.
* **[!UICONTROL Approved]**: Deze sjabloon is zichtbaar voor alle Workfront Fusion-gebruikers op het tabblad [!UICONTROL Public templates] . U kunt een deelbare koppeling ook kopiëren door op [!UICONTROL Options] in de rechterbovenhoek van het scherm te klikken.

U kunt de status ook controleren via de tab [!UICONTROL Team templates] . Als een sjabloon wordt gepubliceerd, heeft deze rechts van de sjabloonnaam een pictogram.

* **het pictogram van het Oogje**: Het malplaatje wordt gepubliceerd; het is zichtbaar slechts voor het team; en een goedkeuringsverzoek werd niet verzonden.
* **Geel controletekenpictogram**: Het malplaatje wordt gepubliceerd; het is zichtbaar slechts voor het team; en het is goedkeuring in afwachting om aan de Openbare malplaatjes tabel worden toegevoegd.
* **Groen controletekenpictogram**: Het malplaatje is beschikbaar in het Openbare malplaatjes tabel en is zichtbaar voor om het even welke gebruiker van de Fusie van Workfront. De eigenschap is ook zichtbaar op het tabblad [!UICONTROL Team templates] . De sjabloonauteur of zijn teamlid kan de sjabloon nog steeds bewerken.

Sjablonen zonder pictogrammen hebben de status [!UICONTROL Private] . Ze worden niet gepubliceerd en zijn alleen zichtbaar voor het team.


<!--

## Questions about how this works

Editing

1. If an admin edits a template, do they have to publish again? ... Do they have to approve again?
1. What does publishing actually do?
1. Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
1. What is the admin approving? Does a user have to submit it for approval? 



What does "Publishing" mean?
What does "Approving" mean?
If an admin edits a template, do they have to publish again? ... Do they have to approve again?
Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
What is the admin approving? Does a user have to submit it for approval?

-->
