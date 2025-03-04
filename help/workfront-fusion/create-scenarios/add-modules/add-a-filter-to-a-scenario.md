---
title: Een filter toevoegen aan een scenario
description: In sommige scenario's, moet u slechts met bundels werken die aan specifieke criteria voldoen. Met filters kunt u deze bundels selecteren.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---

# Een filter toevoegen aan een scenario

In sommige scenario&#39;s, moet u slechts met bundels werken die aan specifieke criteria voldoen. Met filters kunt u deze bundels selecteren.

U kunt bijvoorbeeld een scenario maken met de trigger [!UICONTROL Watch records] voor [!DNL Workfront] om alleen taken vast te leggen die aan een specifieke gebruiker zijn toegewezen.

U kunt een filter tussen twee modules toevoegen en controleren of de bundels die van de voorafgaande modules worden ontvangen specifieke filtervoorwaarden vervullen:

* Als zij, de bundels overgaan tot de volgende module in het scenario.
* Als ze dat niet doen, wordt de verwerking voor de bundels beëindigd.

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

U moet beide modules aan een scenario toevoegen alvorens u een filter tussen hen kunt toevoegen.

## Voeg een filter tussen twee modules toe:

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waaraan u een filter wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik het moersleutelpictogram ![ pictogram van de Sleutel ](assets/wrench-icon.png) tussen de modules waar u een filter wilt toevoegen en **Opstelling een filter** selecteren.
1. Voer in het vak dat wordt weergegeven een **[!UICONTROL Label]** voor het filter in.
1. Definieer het filter **[!UICONTROL Condition]** .

   Typ het veld waarop u wilt filteren in het eerste veld, de operator en (indien nodig) de waarde waarmee u het veld wilt vergelijken.

   >[!TIP]
   >
   >U kunt waarden invoeren in filtervelden vanuit het deelvenster Toewijzing
   >Voor meer informatie bij afbeelding, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   Als u bijvoorbeeld wilt dat het filter bestanden doorgeeft in [!DNL Adobe Workfront] die eindigen met XML, typt u **[!UICONTROL File name]** in het eerste vak en.**[!UICONTROL xml]** in het tweede vak. In het vervolgkeuzemenu ertussen selecteert u **[!UICONTROL Ends with (case insensitive)]** . Dit filter wordt toegepast op binnenkomende bundels uit de eerste module (Workfront). Alleen pakketten met XML-bestanden worden doorgegeven aan de volgende module.

   ![ Opstelling een filter ](assets/set-up-filter-box.png)

1. Klik op **[!DNL OK]**.

## Een filter kopiëren

Momenteel, omvat de scenario redacteur geen eigenschap voor het kopiëren van een filter.

>[!NOTE]
>
>Als u de modules aan weerszijden van het filter kopieert, wordt het filter ook gekopieerd.
>
>Voor meer informatie bij het kopiëren van modules, zie [ modules of scenario&#39;s van het Exemplaar in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

Als u een filter wilt kopiëren zonder modules te kopiëren, kunt u het gereedschap Fusion Dev gebruiken

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waaraan u een filter wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Open Fusion DevTool door op het DevTool pictogram ![ te klikken DevTool pictogram ](assets/debugger-icon.png) dichtbij de bodem van het scherm.

   Als u niet het DevTool pictogram ziet, zie [ zuivert een scenario ](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) voor instructies bij het openen van DevTool.

1. Klik het **[!UICONTROL Tools]** pictogram ![ DevTool hulpmiddelen ](assets/devtools-tools-icon.png) in de linkerzijbar.

1. Klik op **[!UICONTROL Copy Filter]** en configureer het gereedschap **[!UICONTROL Copy Filter]** in het rechterdeelvenster:

   1. Stel de **[!UICONTROL Source Module]** rechtstreeks na het filter dat u wilt kopiëren in als de module.
   1. Stel de **[!UICONTROL Target Module]** in als de module waarna u het filter direct wilt plaatsen.

1. Klik op **[!UICONTROL Run]**.
