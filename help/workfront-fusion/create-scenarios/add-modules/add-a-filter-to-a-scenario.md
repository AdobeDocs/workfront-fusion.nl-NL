---
title: Een filter toevoegen aan een scenario
description: In sommige scenario's, moet u slechts met bundels werken die aan specifieke criteria voldoen. Met filters kunt u deze bundels selecteren.
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: a871a130a1ac023dcb4ce8da7241918da2431d3a
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---

# Een filter toevoegen aan een scenario

In sommige scenario&#39;s, moet u slechts met bundels werken die aan specifieke criteria voldoen. Met filters kunt u deze bundels selecteren.

U kunt bijvoorbeeld een scenario maken met de trigger [!UICONTROL Watch records] voor Workfront om alleen taken vast te leggen die aan een specifieke gebruiker zijn toegewezen.

U kunt een filter tussen twee modules toevoegen en controleren of de bundels die van de voorafgaande modules worden ontvangen specifieke filtervoorwaarden vervullen:

* Als zij, de bundels overgaan tot de volgende module in het scenario.
* Als ze dat niet doen, wordt de verwerking voor de bundels beëindigd.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Elk Adobe Workfront Workflow-pakket en elk Adobe Workfront Automation and Integration-pakket</p><p>Workfront Ultimate</p><p>Workfront Prime en Select packages, met extra aanschaf van Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licenties</td> 
   <td> <p>Standard</p><p>Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Vereisten

U moet beide modules aan een scenario toevoegen alvorens u een filter tussen hen kunt toevoegen.

## Voeg een filter tussen twee modules toe:

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waaraan u een filter wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Klik het moersleutelpictogram ![&#x200B; pictogram van de Sleutel &#x200B;](assets/wrench-icon.png) tussen de modules waar u een filter wilt toevoegen en **Opstelling een filter** selecteren.
1. Voer in het vak dat wordt weergegeven een **[!UICONTROL Label]** voor het filter in.
1. Definieer het filter **[!UICONTROL Condition]** .

   Typ het veld waarop u wilt filteren in het eerste veld, de operator en (indien nodig) de waarde waarmee u het veld wilt vergelijken.

   >[!TIP]
   >
   >U kunt waarden invoeren in filtervelden vanuit het deelvenster Toewijzing
   >Voor meer informatie bij afbeelding, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

   Als u bijvoorbeeld wilt dat het filter bestanden doorgeeft in Adobe Workfront die eindigen met XML, typt u **[!UICONTROL File name]** in het eerste vak en.**[!UICONTROL xml]** in het tweede vak. In het vervolgkeuzemenu ertussen selecteert u **[!UICONTROL Ends with (case insensitive)]** . Dit filter wordt toegepast op binnenkomende bundels uit de eerste module (Workfront). Alleen pakketten met XML-bestanden worden doorgegeven aan de volgende module.

   ![&#x200B; Opstelling een filter &#x200B;](assets/set-up-filter-box.png)

1. Klik op **[!DNL OK]**.

## Een filter kopiëren

Momenteel, omvat de scenario redacteur geen eigenschap voor het kopiëren van een filter.

>[!NOTE]
>
>Als u de modules aan weerszijden van het filter kopieert, wordt het filter ook gekopieerd.
>
>Voor meer informatie bij het kopiëren van modules, zie [&#x200B; modules of scenario&#39;s van het Exemplaar in de Fusie van Adobe Workfront &#x200B;](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

Als u een filter wilt kopiëren zonder modules te kopiëren, kunt u het gereedschap Fusion Dev gebruiken

1. Klik op de tab **[!UICONTROL Scenarios]** in het linkerdeelvenster.
1. Selecteer het scenario waaraan u een filter wilt toevoegen.
1. Klik overal op het scenario om de redacteur van het Scenario in te gaan.
1. Open Fusion DevTool door op het DevTool pictogram ![&#x200B; te klikken DevTool pictogram &#x200B;](assets/debugger-icon.png) dichtbij de bodem van het scherm.

   Als u niet het DevTool pictogram ziet, zie [&#x200B; zuivert een scenario &#x200B;](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) voor instructies bij het openen van DevTool.

1. Klik het **[!UICONTROL Tools]** pictogram ![&#x200B; DevTool hulpmiddelen &#x200B;](assets/devtools-tools-icon.png) in de linkerzijbar.

1. Klik op **[!UICONTROL Copy Filter]** en configureer het gereedschap **[!UICONTROL Copy Filter]** in het rechterdeelvenster:

   1. Stel de **[!UICONTROL Source Module]** rechtstreeks na het filter dat u wilt kopiëren in als de module.
   1. Stel de **[!UICONTROL Target Module]** in als de module waarna u het filter direct wilt plaatsen.

1. Klik op **[!UICONTROL Run]**.
