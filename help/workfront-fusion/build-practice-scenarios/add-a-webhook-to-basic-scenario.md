---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Webhaak toevoegen aan een basisscenario
description: Webhooks, ook wel 'instant triggers' genoemd, zijn een specifiek type triggermodule dat een scenario kan starten wanneer een wijziging wordt aangebracht in plaats van volgens een bepaald schema.
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Webhaak toevoegen aan een basisscenario

Webhooks, ook wel &#39;instant triggers&#39; genoemd, zijn een specifiek type triggermodule dat een scenario kan starten wanneer een wijziging wordt aangebracht in plaats van volgens een bepaald schema.

In dit voorbeeld, zult u een website toevoegen om een scenario te beginnen zodra om het even welke verzoeken aan een specifieke verzoekrij zijn voorgelegd. Het scenario zet dan die verzoeken in een project om.

Dit voorbeeld wijzigt het scenario dat in [ wordt gecreeerd leidt tot een basisscenario ](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md).

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

U moet het scenario tot stand brengen dat in [ wordt beschreven leidt tot een basisscenario ](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md) alvorens deze procedure te volgen.

## Webhaak toevoegen en configureren


### De module Webhaak toevoegen

1. Open het scenario in de scenarioredacteur.
1. Klik op de eerste module met de rechtermuisknop aan en selecteer **module van de Schrapping**.

   De module wordt verwijderd en er blijft een lege tijdelijke aanduiding achter.

1. Klik de lege module, en selecteer **Adobe Workfront** van de lijst van apps.
1. Selecteer **Gebeurtenissen van het Controle**.
1. Klik **toevoegen** naast het gebied van de Webhaak.
1. op het gebied van het Type van Verslag, uitgezochte **Uitgave**, zodat zal de module voor veranderingen in kwesties teweegbrengen.
1. Op het gebied van de Staat, uitgezochte **Nieuwe staat**. Dit is een verplicht veld dat wordt gebruikt voor het filter, dat in dit voorbeeld niet wordt weergegeven.
1. Op het gebied van de Oorsprong van het Verslag, selecteer **Nieuw slechts Verslag**. Dit staat het scenario toe om te teweegbrengen wanneer een kwestie wordt toegevoegd, niet wanneer men wordt bijgewerkt of geschrapt.
1. Klik **sparen** om de moduleconfiguratie te bewaren.

## De tweede module bijwerken

1. Open het scenario.
1. Klik de **objecten van de Bekeerling** module om het te openen.
1. Verwijder het zwarte-id-blok in het veld Uitgave-id. Het blok is zwart omdat de module waarvan het is toegewezen niet meer beschikbaar is.
1. Selecteer het blok van identiteitskaart onder de eerste module (de Gebeurtenissen van het Controle) om het aan de tweede module in kaart te brengen.
1. Klik **OK**.



### Testen en activeren

1. Klik op **[!UICONTROL Run once]** in de linkerbenedenhoek van de scenarioeditor.

   Het scenario moet lopen om op het nieuwe verzoek te letten.
1. Ga naar de Workfront-omgeving waarmee Fusion verbinding maakt en voeg een probleem toe.

   Het scenario moet worden uitgevoerd.
1. Onderzoek de output om ervoor te zorgen dat het scenario zoals verwacht liep.
1. Wanneer u wordt tevreden dat het scenario zoals verwacht werkt, klik **plannend** knevel in laag-linkervan het scherm aan ****.

   Dit activeert het scenario.
1. Klik in [!DNL Workfront Fusion] in de linkerbenedenhoek op **[!UICONTROL Save]** om de voortgang van het scenario op te slaan.
