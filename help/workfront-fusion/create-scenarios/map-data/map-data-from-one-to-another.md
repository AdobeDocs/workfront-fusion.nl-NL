---
title: De informatie van de kaart van één module aan een andere
description: Toewijzing is het proces om de output van een module, gestructureerd in punten, aan de inputgebieden van een andere module toe te wijzen.
author: Becky
feature: Workfront Fusion
exl-id: 1e3f7729-f48e-451e-a90b-d680c9e3bcbc
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# De informatie van de kaart van één module aan een andere

Toewijzing is het toewijzen van de uitvoer van een module aan de invoervelden van een andere module.

Het deelvenster Toewijzing wordt weergegeven wanneer u op een veld klikt waarin u een waarde kunt invoegen die is uitgevoerd vanuit een voorgaande module in een scenario.

U kunt ook een formule maken met een willekeurige combinatie van functies en toegewezen items in het deelvenster Toewijzing met statische tekst die u typt. Deze elementen kunnen in elkaar worden genest.

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

## Een item toewijzen

Nadat u een opeenvolging van modules door twee of meer van hen te verbinden hebt gecreeerd, kan elke module waarden van punten verwerken die door de modules worden uitgevoerd die het voorafgaan.

Uitvoeritems toewijzen aan de invoervelden van een module:

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waarin u gegevens wilt toewijzen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik op de module die de output van de voorafgaande module of modules zou moeten verwerken.
1. Klik in het deelvenster Moduleinstellingen dat wordt weergegeven op een veld waarin u de waarde wilt gebruiken van een item dat is uitgevoerd vanuit een vorige module.

   Het deelvenster Toewijzing wordt geopend.

1. (Optioneel) Als u naar een bepaald veld in het deelvenster Toewijzing wilt zoeken, klikt u op de zoekbalk van het deelvenster Toewijzing en typt u de term die u wilt zoeken. Klik op het veld wanneer dit in de lijst wordt weergegeven.

   Zoekresultaten bevatten de zoekterm en zijn niet hoofdlettergevoelig.
1. Als u een waarde wilt selecteren die een element van een verzameling is, klikt u op de pijl naast die verzameling en selecteert u vervolgens het element wanneer dat wordt weergegeven.

   ![&#x200B; element van de Inzameling &#x200B;](assets/collection-dropdown.png)

1. Klik op een item in het deelvenster Toewijzing om het in te voegen in het veld.

Voor meer informatie, zie [&#x200B; een module &#x200B;](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md) vormen.


## Problemen oplossen

### Probleem: ontbrekende items in het deelvenster Toewijzing

In het deelvenster Toewijzing worden de uitvoeritems van vorige modules weergegeven. Soms ontbreken bepaalde items in dit deelvenster. U kunt de module in werking stellen die output in de scenarioredacteur mist, en het toewijzingspaneel kan die punten in recentere modules dan omvatten. De nauwkeurige procedure verschilt afhankelijk van het type van de module

* [Instant trigger](#instant-trigger)
* [Opiniepeilingtrigger](#polling-trigger)
* [Overige modules](#other-modules)

#### Instant trigger

1. Klik met de rechtermuisknop op de module en klik vervolgens op **[!UICONTROL Run this module only]** in het menu dat wordt weergegeven.

   Omdat dit een instant trigger is, begint het te kijken naar gebeurtenissen.

1. Maak de gebeurtenis die in de module wordt bekeken.

   Als de module bijvoorbeeld een module is van Workfront > Watch Events die op taaktoewijzingen controleert, meldt u zich aan bij Workfront (als een gebruiker die niet de gebruiker is die de Fusion-verbinding gebruikt) en wijst u een taak toe.

1. Wanneer de module eindigt lopend, klik de bel boven de module om zijn volledige output te onderzoeken.

   Het deelvenster Toewijzing voor latere modules bevat nu alle items in de uitvoer van de module.

#### Opiniepeilingtrigger

1. Klik met de rechtermuisknop op de module en klik vervolgens op **[!UICONTROL Run this module only]** in het menu dat wordt weergegeven.
1. Als er geen uitvoer is, klikt u op **[!UICONTROL Choose where to start]** en past u de instellingen aan.
1. (Voorwaardelijk) Als er geen gebeurtenis is die moet worden verwerkt, maakt u de gebeurtenis die in de module wordt gecontroleerd en herhaalt u stap 2.

   Bijvoorbeeld, als de module een Workfront > module van het Horloge- verslagen is die voor taaktaken letten, login in Workfront (als gebruiker die niet de gebruiker is die de verbinding van de Fusie gebruikt) en een taak toewijst, dan stel opnieuw de module in werking.

1. Wanneer de module eindigt lopend, klik de bel boven de module om zijn volledige output te onderzoeken.

   Het deelvenster Toewijzing voor latere modules bevat nu alle items in de uitvoer van de module.

#### Overige modules

U kunt kiezen om uit te voeren:

* Het hele scenario (of alleen het onderdeel dat de module bevat)
* De enige module

De enige module uitvoeren:

1. Klik met de rechtermuisknop op de module en klik vervolgens op **[!UICONTROL Run this module only]** in het menu dat wordt weergegeven.
1. Geef voorbeeldwaarden op voor de invoeritems en klik op **[!UICONTROL OK]** .
1. Wanneer de module eindigt lopend, klik de bel boven de module om zijn volledige output te onderzoeken.

   Het deelvenster Toewijzing voor latere modules bevat nu alle items in de uitvoer van de module.
