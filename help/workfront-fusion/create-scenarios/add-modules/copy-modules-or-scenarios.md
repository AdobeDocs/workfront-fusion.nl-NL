---
title: Modules of scenario's kopiëren
description: U kunt modules, groepen modules, of volledige scenario's in de Fusie van Adobe Workfront kopiëren. Deze capaciteit staat u toe om scenario's of delen van scenario's opnieuw te gebruiken zonder het moeten hen opnieuw bouwen.
author: Becky
feature: Workfront Fusion
exl-id: 5cece7d4-b2c7-4276-8a6f-f65bad799c7a
source-git-commit: 860209fdcf2e7707663cc2d454c0499972b1261e
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Modules of scenario&#39;s kopiëren

U kunt modules, groepen modules, of volledige scenario&#39;s in de Fusie van Adobe Workfront kopiëren. Deze capaciteit staat u toe om scenario&#39;s of delen van scenario&#39;s opnieuw te gebruiken zonder het moeten hen opnieuw bouwen.

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

De modules moeten in een scenario bestaan alvorens u hen kunt kopiëren.

## Een module of een groep modules kopiëren

Wanneer u een module kopieert, behoudt de kopie alle veldwaarden en instellingen van de originele module.

U kunt de module of modules in een ander gebied van het zelfde scenario, of in een verschillend scenario kleven.

Overweeg het volgende wanneer het kleven van modules in een verschillend scenario:

* Veldwaarden die gegevens ophalen uit een andere module die u niet hebt gekopieerd, hebben geen toegang meer tot die gegevens. U moet deze gebieden plaatsen om informatie uit het nieuwe scenario te trekken.
* Als u de modules in een scenario kleeft dat door een ander team of een organisatie wordt bezeten, moeten alle verbindingen aan verbindingen worden bijgewerkt die door het team of de organisatie worden bezeten die het nieuwe scenario bezit.

### Modules kopiëren

Het kopiëren van een groep modules is vergelijkbaar met het kopiëren van één module.

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waar u een module wilt kopiëren.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik met de rechtermuisknop op de module die u wilt kopiëren.

   >[!NOTE]
   >
   >U kunt meer dan één module selecteren door [!UICONTROL shift] te houden en op de modules te klikken die u wilt kopiëren. Het kopiëren van een groep modules kopieert ook om het even welke verbindende lijnen, filters, of het verpletteren van logica tussen hen.

1. Selecteer **[!UICONTROL Copy module]** .
1. Verplaats de curseur naar het gebied van het scenario waar u het exemplaar van het scenario wilt.
1. Klik met de rechtermuisknop en selecteer **[!UICONTROL Paste]** .
1. Sluit de geplakte modules aan op het scenario door deze naar de juiste locatie in het scenario te slepen.

   U kunt ook met sneltoetsen kopiëren en plakken.

## Een scenario kopiëren door te klonen

Het klonen van een scenario leidt tot een exemplaar van het scenario, dat u dan kunt uitgeven.

1. Open de pagina met de details van het scenario:

   1. Klik op de tab **[!UICONTROL Scenario]** in het linkerdeelvenster en klik op een scenario waarin u details wilt weergeven.

      of

      Als u aan het scenario in de scenario redacteur werkt, klik de linkerpijl ![ Uitgaan die pijl ](assets/exit-editing-arrow.png) dichtbij de upper-left hoek van het venster uitgeeft.

1. Klik met de rechtermuisknop **[!UICONTROL Options]** rechtsboven op de pagina.
1. Selecteer **[!UICONTROL Clone]** .
1. (Optioneel) Voer een naam in voor het nieuwe scenario.
1. (Optioneel) Schakel **[!UICONTROL Keep the states of any new modules the same as those being duplicated]** in om ervoor te zorgen dat het gekopieerde scenario ook informatie bevat over de meest recente records die door het oorspronkelijke scenario zijn verwerkt.
1. Klik op **[!UICONTROL Save]** om het scenario te maken.

## Een scenario kopiëren met behulp van blauwdrukken

Scenario-blauwdrukken vertegenwoordigen de rangschikking, toewijzing en veldwaarden van een bepaald scenario op een bepaald tijdstip. U kunt een scenario-blauwdruk naar een JSON-bestand op uw computer exporteren en het vervolgens importeren wanneer u een nieuw scenario maakt. Scenario&#39;s die uit een scenario-blauwdruk zijn geïmporteerd, kunnen worden bewerkt.

Een scenario blauwdruk vertegenwoordigt het volledige scenario. Als u slechts bepaalde modules van een scenario wilt kopiëren, zie [ een module of een groep modules ](#copy-a-module-or-a-group-of-modules) in dit artikel kopiëren.

### Een scenario-blauwdruk exporteren

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waarin u een blauwdruk wilt exporteren.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik in het scenario op het menu **[!UICONTROL More]** in het gebied met scenario-instellingen.
1. Klik op **[!UICONTROL Export Blueprint]**.

   Er wordt een JSON-bestand gemaakt en gedownload naar de computer. U kunt dit bestand zoeken in de map [!DNL Downloads] .

>[!NOTE]
>
>Om de blauwdruk voor een vorige versie van een scenario uit te voeren, zie [ Mening en beheer scenario versies ](/help/workfront-fusion/manage-scenarios/restore-a-scenario-version.md).

### Een blauwdruk importeren

>[!IMPORTANT]
>
>Als u een blauwdruk in een bestaand scenario invoert, vervangt het scenario blauwdruk het bestaande scenario. U kunt geen blauwdruk aan een bestaand scenario toevoegen.

1. Beginnen met het maken van een nieuw scenario.
1. Klik in het scenario op het menu **[!UICONTROL More]** in het gebied met scenario-instellingen.
1. Klik op **[!UICONTROL Import Blueprint]**.
1. Klik in het dialoogvenster dat wordt weergegeven op **[!UICONTROL Browse]**
1. Navigeer naar de blauwdruk die u wilt importeren en klik op **[!UICONTROL Open]** .
1. Klik op **[!UICONTROL Save]**.

   Er wordt een JSON-bestand gemaakt en gedownload naar de computer. U kunt dit bestand zoeken in de map [!UICONTROL Downloads] .

## De scenario&#39;s van het exemplaar en hergebruik door malplaatjes te gebruiken

U kunt sjablonen maken als beginpunt voor uw [!DNL Workfront Fusion] -scenario&#39;s. Wanneer u een scenario van een malplaatje creeert, kunt u het scenario wijzigen zonder het malplaatje te wijzigen. Veldwaarden worden niet opgeslagen in sjablonen.

Voor meer informatie bij het creëren van een scenario gebruikend een malplaatje, zie [ scenario&#39;s met malplaatjes ](/help/workfront-fusion/create-scenarios/add-modules/create-scenarios-with-fusion-templates.md) creëren.

## Problemen oplossen

Als u kopieert en modules zoals die in [ wordt beschreven Kopieer een module of een groep modules ](#copy-a-module-or-a-group-of-modules) kleeft en niets wanneer u kleeft, controleer de de plaatsmontages van uw browser om ervoor te zorgen dat het kleven van het klembord wordt toegestaan.
