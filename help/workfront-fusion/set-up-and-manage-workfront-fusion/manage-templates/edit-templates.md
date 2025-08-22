---
content-type: reference
title: Sjablonen bewerken
description: In dit artikel wordt beschreven hoe u Fusion-sjablonen kunt bewerken.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 473dba8b-faa4-432f-9357-c2146e86b261
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Sjablonen bewerken

Adobe Workfront Fusion-sjablonen zijn vooraf ontwikkelde scenario&#39;s die zijn ontworpen om verschillende workflows te automatiseren en te stroomlijnen. Met deze sjablonen kunt u snel integratie en automatisering instellen zonder dat u alles helemaal zelf hoeft te bouwen.

Als beheerder hebt u toestemming om sjablonen die door anderen zijn gemaakt, weer te geven, te wijzigen, te hernoemen, te publiceren, goed te keuren en te verwijderen.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">Adobe Workfront-plan</td>
      <td><p>Alle</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">Adobe Workfront-licentie</td>
      <td><p>Nieuw: Standaard</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p></td>
    </tr>
    <tr>
      <td role="rowheader">Adobe Workfront Fusion-licentie**</td>
      <td>
        <p>Huidig: Geen Workfront Fusion-licentievereisten.</p>
        <p>of</p>
        <p>Verouderd: alle</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Product</td>
      <td>
        <p>Nieuw:</p>
        <ul>
          <li>[!UICONTROL Select] of [!UICONTROL Prime] Workfront Plan: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li>
          <li>[!UICONTROL Ultimate] Workfront-abonnement: Workfront Fusion is inbegrepen.</li>
        </ul>
        <p>of</p>
        <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md). -->

+++

## Workfront Fusion-sjablonen bewerken als beheerder

1. Klik op **[!UICONTROL Administration]** in het navigatievenster aan de linkerkant om het [!UICONTROL Administration] -gebied te openen.
1. Klik op **[!UICONTROL All Templates]** in het navigatievenster aan de linkerkant.
1. Klik op **[!UICONTROL Detail]** rechts van de sjabloon die u wilt bewerken.
1. (Facultatief) verander het malplaatje door **Opties** in de hoger-juiste hoek te klikken en **te selecteren anders noemen**.
1. (Facultatief) om de taal van uw malplaatje te veranderen, klik **[!UICONTROL Create a new template]** ![ de montagespictogram van het Scenario ](assets/fusion-scenario-settings-icon.png), en selecteer de taal van de drop-down Taal.

   >[!IMPORTANT]
   >
   >De taalselectie komt overeen met de talen die beschikbaar zijn in de systeeminstellingen en heeft alleen betrekking op de naam van de openbare sjabloon en de beschrijving ervan. U kunt een sjabloontaal niet wijzigen nadat de sjabloon is opgeslagen.

1. (Facultatief) om de malplaatjebeschrijving uit te geven, klik **[!UICONTROL Set up a template]** ![ de montagespictogram van het Scenario ](assets/fusion-scenario-settings-icon.png), en ga de beschrijving in.
1. U kunt apps, modules en gereedschappen op dezelfde manier toevoegen of bewerken als bij het maken van een standaardscenario.

   Om contextafhankelijke hulp aan de modules toe te voegen, zie [ Opstelling [!UICONTROL Wizard] functionaliteit ](#set-up-wizard-functionality) in dit artikel.

   <!--For more information on building a scenario, see [Create a scenario in Adobe Workfront Fusion](../../../workfront-fusion/scenarios/create-a-scenario.md).-->

   >[!NOTE]
   >
   >Als uw malplaatje modules omvat die vereisen toevoegend de verbinding, geloofsbrieven, of andere privacy-gevoelige informatie, wordt deze informatie niet gedeeld met de malplaatjegebruikers.

1. (Optioneel) Klik op **[!UICONTROL Run once]** om de sjabloon te testen.
1. Klik het **[!UICONTROL Save]** pictogram ![ sparen pictogram ](assets/save-icon.png).


## [!UICONTROL Wizard] -functionaliteit instellen

Met [!DNL Workfront Fusion template] [!UICONTROL Wizard] kunt u toekomstige gebruikers van de sjabloon instructies of informatie geven over de specifieke velden die in modules worden gebruikt.

1. Klik op de module die aan de sjabloon is toegevoegd om de velden van de module weer te geven.
1. Zoek het veld waar u [!UICONTROL Wizard] informatie wilt toevoegen en schakel **[!UICONTROL Use in Wizard]** onder dat veld in.
1. Voer in het veld [!UICONTROL Help] de informatie in die u voor gebruikers zichtbaar wilt maken.
1. (Optioneel) Schakel **[!UICONTROL Use as default value]** in als u wilt dat gebruikers deze tekst kunnen zien wanneer ze de sjabloon gebruiken.
1. Herhaal stap 2-4 voor elk veld waarvoor u informatie wilt opgeven.
1. Klik op **[!UICONTROL OK]** om de wijzigingen op te slaan en de module te sluiten.

Het publicatieproces is hetzelfde als in het geval van een standaardgebruiker. Voor informatie, zie [ publiceren en delen malplaatjes ](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md) sectie voor meer details.

## Sjabloonstatussen

U kunt de status op de sjabloonpagina onder de sjabloonnaam controleren.

De volgende statussen zijn beschikbaar:

* **[!UICONTROL Private]**: Deze sjabloon is alleen zichtbaar voor de sjabloonauteur en zijn team.
* **[!UICONTROL Published]**: Deze sjabloon is alleen zichtbaar voor de sjabloonauteur en zijn team. Na publicatie kunt u de sjabloon desgewenst ter goedkeuring verzenden. U kunt ook een deelbare koppeling kopiëren.
* **[!UICONTROL Approved]**: Deze sjabloon is zichtbaar voor alle Workfront Fusion-gebruikers op het tabblad [!UICONTROL Public templates] . U kunt een deelbare koppeling ook kopiëren door op [!UICONTROL Options] in de rechterbovenhoek van het scherm te klikken.

U kunt de status ook controleren via de tab [!UICONTROL Team templates] . Als een sjabloon wordt gepubliceerd, heeft deze rechts van de sjabloonnaam een pictogram.

* **het pictogram van het Oogje**: Het malplaatje wordt gepubliceerd; het is zichtbaar voor het team.
* **Geel controletekenpictogram**: Het malplaatje wordt gepubliceerd; het is zichtbaar slechts voor het team; en het is goedkeuring in afwachting om aan de Openbare malplaatjes tabel worden toegevoegd.
* **Groen controletekenpictogram**: Het malplaatje is beschikbaar in het Openbare malplaatjes tabel en is zichtbaar voor om het even welke gebruiker van de Fusie van Workfront. De eigenschap is ook zichtbaar op het tabblad [!UICONTROL Team templates] . De sjabloonauteur of zijn teamlid kan de sjabloon nog steeds bewerken.

Sjablonen zonder pictogrammen hebben de status [!UICONTROL Private] . Ze worden niet gepubliceerd en zijn alleen zichtbaar voor het team.

## SVG-gegevens van een sjabloon zoeken

1. Klik op **[!UICONTROL Administration]** in het navigatievenster aan de linkerkant om het [!UICONTROL Administration] -gebied te openen.
1. Klik op **[!UICONTROL Templates]** in het navigatievenster aan de linkerkant.
1. Klik op de sjabloon waarvoor u informatie wilt zoeken.
1. Klik **Opties** in de hoger-juiste hoek.
1. Selecteer *Diagram van SVG*.

Hier kunt u het SVG-diagram en de SVG-code bekijken.
