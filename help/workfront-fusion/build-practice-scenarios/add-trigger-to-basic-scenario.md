---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: Een triggermodule toevoegen aan een basisscenario
description: Leer hoe te om een trekkermodule toe te voegen om het scenario toe te staan om periodiek naar nieuwe verzoeken te zoeken en hen in projecten om te zetten.
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
source-git-commit: 8884aef2237ad358c774110b81ac17b9efb386d4
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---

# Een triggermodule toevoegen aan een basisscenario

De triggermodules worden aan het begin van een scenario geplaatst. Deze modules beginnen een scenario uitvoering wanneer er een verandering in een bepaalde dienst is geweest. De wijziging kan bestaan uit het maken van nieuwe records, het verwijderen van records, het bijwerken van records, enzovoort. U geeft de criteria op voor de wijzigingen die met het scenario beginnen.

De modules van de opiniepeiling controleren de dienst bij een vastgestelde tijdinterval en keren informatie over veranderingen terug die tijdens dat tijdinterval voorkwamen. Als er geen veranderingen zijn geweest, voert de trekker niet het scenario uit.

In dit voorbeeld, zult u een trekkermodule toevoegen die om de 15 minuten in werking stelt en begint een scenario als om het even welke verzoeken aan een specifieke rij zijn voorgelegd. Het scenario zet dan die verzoeken in een project om.

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

## De triggermodule toevoegen en configureren

### De triggermodule toevoegen

1. Open het scenario in de scenarioredacteur.
1. Klik op de eerste (Onderzoek) module met de rechtermuisknop aan en selecteer **module van de Schrapping**.

   De module wordt verwijderd en er blijft een lege tijdelijke aanduiding achter.

1. Klik de lege module, en selecteer **Adobe Workfront** van de lijst van apps.
1. Selecteer **Verslag van het Controle**.
1. Zorg ervoor dat de module de zelfde verbinding zoals de rest modules in het scenario gebruikt.
1. Op het gebied van het Type van Verslag, uitgezochte **Uitgave**.
1. Op het gebied van de Filter, uitgezochte **Alleen Nieuwe Verslagen**.
1. Selecteer `ID`, `Name` en `Project ID` in het vak Uitvoer.
1. Klik **O.K.** om de modulemontages te bewaren.

   Er verschijnt een venster waarin u wilt beginnen.

1. Selecteer **van nu op**.

### De triggermodule inplannen

1. Klik op de klok in de module Controleverslagen.

   Het venster Schema-instelling wordt geopend.

1. Op het het scenario van de Looppas gebied, selecteer **met regelmatige intervallen**.

1. Klik **OK**.

### De tweede module bijwerken

Omdat de eerste module is vervangen, moet de tweede module aan de nieuwe eerste module worden in kaart gebracht.

1. Open de module Object omzetten.
1. Verwijder het zwarte-id-blok in het veld Uitgave-id. Het blok is zwart omdat de module waarvan het is toegewezen niet meer beschikbaar is.
1. Selecteer het blok van identiteitskaart onder de eerste module (de Verslagen van het Controle) om het aan de tweede module in kaart te brengen.
1. Klik **OK**.

### Testen en activeren

1. Ga naar de Workfront-omgeving waarmee Fusion verbinding maakt en voeg een probleem toe.
1. Klik op **[!UICONTROL Run once]** in de linkerbenedenhoek van de scenarioeditor.
1. Onderzoek de output om ervoor te zorgen dat het scenario zoals verwacht liep.
1. Wanneer u wordt tevreden dat het scenario zoals verwacht werkt, klik **plannend** knevel in laag-linkervan het scherm aan ****.

   Dit activeert het scenario.
1. Klik in [!DNL Workfront Fusion] in de linkerbenedenhoek op **[!UICONTROL Save]** om de voortgang van het scenario op te slaan.

   >[!IMPORTANT]
   >
   >Sla de bestanden vaak op terwijl u ze gebruikt en test een scenario.

## Bronnen

* Voor meer informatie over trekkermodules, zie [ modules van de Trekker ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) in het overzicht van de artikelmodules.
