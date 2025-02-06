---
title: Workflow voor het maken van een scenario
description: Volg deze algemene workflow om een scenario te maken
author: Becky
feature: Workfront Fusion
exl-id: 49f8edd7-e29a-4ead-9134-a9f0d1cc244d
source-git-commit: c34adf455ce01da52c321d3f997a58f8251d97bf
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Workflow voor het maken van een scenario

De scenario&#39;s worden gebouwd om aan de behoeften van uw organisatie, met toepassingen en modules te voldoen die uw gebruiksgevallen richten. Het maken van een scenario volgt echter dezelfde basisworkflow, ongeacht het gebruik. Dit artikel beschrijft het basisproces om een scenario tot stand te brengen.


* [Het scenario maken en een naam geven](#create-and-name-the-scenario)
* [De eerste module toevoegen en configureren](#configure-the-first-module)
* [Verbindingen maken](#create-connections)
* [Extra modules toevoegen en configureren](#add-and-configure-additional-modules)
* [Gegevens toewijzen tussen modules](#map-data-between-modules)
* [Vorm het verpletteren](#configure-routing)
* [Foutafhandeling configureren](#configure-error-handling)
* [Scenario-instellingen configureren](#onfigure-scenario-settings)
* [Testen en herzien](#test-and-revise)
* [Het scenario activeren](#activate-the-scenario)

Sneltoetsen



## Het scenario maken en een naam geven

1. Meld u aan bij uw [!DNL Workfront Fusion] -account.
1. Klik **[!UICONTROL Scenarios]** {het pictogram van 1} Scenario&#39;s ](assets/scenarios-icon.png) in het linkerpaneel.![

   >[!NOTE]
   >
   >Als u niet het linkernavigatievenster of zijn pictogrammen ziet, klik het pictogram van het Menu ![ Menu ](assets/main-menu-icon-left-nav.png).

1. (Facultatief) in het [!UICONTROL **paneel van Omslagen**], klik het **[!UICONTROL Add folder]** pictogram ![ voeg omslagpictogram ](assets/add-folder-icon.png) toe, dan typ een naam als &quot;scenario&#39;s van de Praktijk&quot;voor uw eerste omslag.

1. (Optioneel) Open de map en klik vervolgens op **[!UICONTROL Create a new scenario]** rechtsboven op de pagina.

1. Selecteer de naam van de tijdelijke aanduiding **[!UICONTROL New scenario]** in de linkerbovenhoek en typ een naam zoals &quot;Praktisch scenario 1&quot;.

   ![ Naam het scenario ](assets/name-the-scenario.png)

1. Ga met [ verder verbind de eerste module ](#2-connect-the-first-module) hieronder.

## De eerste module toevoegen en configureren

De eerste module voor uw scenario is een trekkermodule, die het scenario zal beginnen wanneer bepaalde voorwaarden worden voldaan aan.

Voor instructies bij het toevoegen van de eerste module aan een scenario, zie [ de eerste module aan een scenario ](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-basic.md#add-the-first-module-to-a-scenario) in het artikel toevoegen een module aan een scenario.

Voor instructies bij het vormen van een module, zie [ een module ](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md) vormen

## Verbindingen maken

Wanneer het vormen van een module, moet u ingaan of een verbinding tot stand brengen. De module gebruikt deze verbinding en de toestemmingen het bevat aan toegangsdatum in de toepassing.

Voor basisinstructies op hoe te om een verbinding tot stand te brengen, zie [ een verbinding tot stand brengen - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

Voor specifieke gebruiksgevallen die Google, Microsoft, of toepassingen zonder specifieke schakelaars impliceren, zie de andere artikelen onder [ verbinden met toepassingen: artikelindex ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-apps-toc.md).

## Extra modules toevoegen en configureren

Ga verder met het toevoegen en configureren van extra modules.

Voor instructies op de manieren om modules toe te voegen, zie de artikelen die onder [ worden vermeld modules toevoegen: artikelindex ](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md).

## Gegevens toewijzen tussen modules

U kunt output van vorige modules als input in verdere modules gebruiken. U kunt bijvoorbeeld een Workfront-project maken in één module en een document uploaden naar die module in een volgende module.

Voor instructies, zie de artikelen onder [ gegevens van de Kaart: artikelindex ](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md).

## Vorm het verpletteren

Het verpletteren staat het scenario toe om verschillende acties uit te voeren die op gegevenswaarden worden gebaseerd.

Voor instructies, zie [ een module van de Router toevoegen en routes ](/help/workfront-fusion/create-scenarios/add-modules/router-module.md) vormen.

## Foutafhandeling configureren

Met foutafhandeling kan het scenario worden hersteld op basis van fouten. U kunt selecteren hoe u het scenario in verschillende foutensituaties wilt reageren.

Voor instructies, zie [ fout behandeling ](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md) toevoegen.

## Scenario-instellingen configureren

U kunt montages voor uw scenario als geheel vormen, zoals het plannen van een scenario, het maken van nota&#39;s, of het bepalen hoe het gegeven wordt opgeslagen.

Voor instructies, zie de artikelen onder [ scenario montages vormen: artikelindex ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/config-scenario-settings-toc.md).

## Testen en herzien

Het testen van uw scenario laat u toe om te bepalen als uw scenario zoals bedoeld werkt. U kunt dan het scenario herzien dat op uw resultaten wordt gebaseerd, en dan opnieuw testen.

1. Klik op **[!UICONTROL Run once]** in de linkerbenedenhoek van de scenarioeditor.
1. Nadat het scenario klaar is met draaien, klikt u op de bellen van de uitvoercontrole boven elke module om de invoer van informatie en de uitvoer van die module te zien.

   * Voor algemene informatie bij het lezen van de informatie van de scenariouitvoering, zie [ de uitvoeringsstroom van het scenario ](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md).
   * Voor informatie over verwerkte bundels, zie [ uitvoering Scenario, cycli, en fasen in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

1. In [!DNL Workfront Fusion], klik **[!UICONTROL Save]** ![ sparen pictogram ](assets/save-icon.png) dichtbij de laag-linkerhoek om uw vooruitgang op het scenario te bewaren.

   >[!IMPORTANT]
   >
   >Sla de bestanden vaak op terwijl u ze gebruikt en test een scenario.

## Het scenario activeren

Dit voorbeeldscenario heeft geen triggermodule. Als dit een scenario zou zijn zou u voor echte gegevens gebruiken het met een trekkermodule beginnen, en het laatste ding u zou doen is het activeren. Nadat u een scenario activeert, door gebrek, loopt het om de 15 minuten. U kunt dit veranderen door te bepalen wanneer en hoe vaak u het wilt lopen.

Voor meer informatie over het activeren van scenario&#39;s, zie [ een scenario ](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md) activeren of deactiveren.

Voor informatie over programma&#39;s, zie [ Plan een scenario ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

## Sneltoetsen voor Workfront Fusion-scenario

U kunt de volgende sneltoetsen gebruiken bij het maken of bewerken van een scenario:

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <thead> 
  <tr> 
   <th> <p>Handeling</p> </th> 
   <th>[!DNL Windows]</th> 
   <th> <p>[!DNL MacOS]</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save] </td> 
   <td>Ctrl+Shift+S</td> 
   <td>Cmd+Shift+S</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Run Once]</td> 
   <td>Ctrl+Shift+Enter</td> 
   <td>Cmd+Shift+Enter </span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Open the DevTool]</td> 
   <td>F12</td> 
   <td>Ctrl+Fn+F12 </span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select multiple modules]</td> 
   <td>Shift+slepen</td> 
   <td>Shift+Drag </span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy]</td> 
   <td>Ctrl+C</td> 
   <td>Cmd+C</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Paste]</td> 
   <td>Ctrl+V</td> 
   <td>Cmd+V</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Plak cURL in scenario om de module HTTP te maken</td> 
   <td colspan="2">Kopieer cURL en plak vervolgens ergens in de scenario-editor.<p>Voor meer informatie, zie <a href="/help/workfront-fusion/create-scenarios/add-modules/use-curl-create-http.md"> Gebruik cURL om een module van HTTP </a> toe te voegen.</td> 
  </tr> 
 </tbody> 
</table>





