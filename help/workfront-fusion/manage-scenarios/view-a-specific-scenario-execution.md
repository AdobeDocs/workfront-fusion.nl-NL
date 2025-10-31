---
title: Een specifieke uitvoering van een scenario weergeven
description: U kunt details van een specifieke scenario uitvoering, met inbegrip van het filtreren en het zoeken naar scenario gebeurtenissen bekijken.
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Een specifieke uitvoering van een scenario weergeven

U kunt details van een specifieke scenario uitvoering, met inbegrip van het filtreren en het zoeken naar scenario gebeurtenissen bekijken.

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

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Een specifieke uitvoering weergeven

U kunt een uitvoering van de het scenariogeschiedenis van het scenario bekijken.


1. Klik op de tab **[!UICONTROL Scenario]** in het linkerdeelvenster en klik vervolgens op het scenario.

   of

   Als u aan het scenario in de redacteur van het Scenario werkt, klik de linkerpijl ![ Uitgang die pijl ](assets/exit-editing-arrow.png) dichtbij de upper-left hoek van het venster uitgeeft.

1. Klik **Geschiedenis** dichtbij de naam van het scenario.
   ![ geschiedenislusje ](assets/history-tab.png)


1. Bepaal de plaats van de uitvoering u wilt bekijken, en **Details** in het uiterste recht op de lijn voor die uitvoering klikken. De koppeling [!UICONTROL details] is alleen zichtbaar als er details beschikbaar zijn voor de uitvoering.

   Het scenario-diagram wordt geopend en het deelvenster met uitvoeringsdetails wordt rechts geopend.

   De modules die output voor deze uitvoering produceerden zijn duidelijk met groene titels.

   Modules die niet zijn uitgevoerd, worden grijs weergegeven.

1. Als u de uitvoer van een module wilt weergeven, klikt u op de uitvoerdetailballon in de buurt van de module. Het aantal in de bel vertegenwoordigt het aantal bundels die de module uitvoert.

   ![ bel van de Output dichtbij een module ](assets/output-bubble.png)

1. Klik op het filter om de bundels weer te geven die door een filter zijn doorgegeven. Het getal bij het filter staat voor het aantal bundels dat door het filter is gegaan.
1. Om naar een specifieke module of een gebeurtenis in het uitvoeringspaneel te zoeken, ga de onderzoekstermijn in de **de uitvoeringsgebeurtenissen van het Onderzoek** doos in. De resultaten worden weergegeven terwijl u typt.
1. Om de onderzoeksresultaten van het uitvoerpaneel door status zoals Succes of Waarschuwing te beperken, klik de **dropdown van de Filter van de Status 0} {en selecteer de status.**




>[!NOTE]
>
>Als u een koppeling naar een specifieke module wilt maken, voegt u `?moduleId=<module-id>` toe aan de URL bij de weergave van de volgende pagina&#39;s:
>
>* Scenario-bewerkingspagina (URL eindigt bij `/edit`)
>* Een specifieke uitvoering van een scène (URL eindigt in `/logs/<log-id>`)
>
>`<module-id>` verwijst naar het getal naast het modulelabel wanneer het scenario wordt weergegeven.
>
>Dit kan nuttig zijn wanneer het zuiveren scenario&#39;s of het kopiëren moduleconfiguratie.
