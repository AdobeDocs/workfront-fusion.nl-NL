---
title: Afbeeldingsmodules
description: Met de Adobe Workfront Fusion Image-modules kunt u informatie ophalen over een bepaalde afbeelding (afmetingen, type, enzovoort), een afbeelding omzetten in een andere bestandsindeling en de grootte van de afbeelding rechtstreeks wijzigen.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
source-git-commit: 3834bb9c7f07e0097783c44558fd656d455337b4
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# Afbeeldingsmodules

[!DNL Adobe Workfront Fusion] [!UICONTROL Image] -modules kunt u informatie ophalen over een bepaalde afbeelding (afmetingen, type, enzovoort), een afbeelding omzetten in een andere bestandsindeling en de grootte van de afbeelding rechtstreeks wijzigen.

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
   <td> <p>Nieuw: Standaard</p><p>of</p><p>Huidig: Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Geen Workfront Fusion-licentievereiste.</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>Select- of Prime Workfront-pakket: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>Ultimate Workfront-pakket: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## [!UICONTROL Image] modules en hun velden

Als u deze module configureert, worden de volgende velden weergegeven. Een bolde titel in een module wijst op een vereist gebied.

* [[!UICONTROL Convert a format]](#convert-a-format)
* [[!UICONTROL Extract metadata]](#extract-metadata)
* [[!UICONTROL Resize]](#resize)

### [!UICONTROL Convert a format]

Deze transformatormodule wijzigt de indeling van een afbeeldingsbestand. Deze module is compatibel met de volgende indelingen:

* PNG
* JPG
* GIF
* BMP

Zowel het bronbestand als de uitvoer moeten een van deze indelingen hebben. Met de module [!UICONTROL Image] > [!UICONTROL Convert a format] kunt u bijvoorbeeld een PNG-bestand omzetten in een BMP-bestand of een BMP in een JPG.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output format]</td> 
   <td>Selecteer de indeling waarin de module het bronbestand moet omzetten. </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Extract metadata]

Deze transformatormodule keert basisinformatie over een module terug.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Resize]

Deze transformatormodule wijzigt de hoogte en breedte van een afbeelding op basis van criteria die u opgeeft.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL I want to]</td> 
   <td>Selecteer of u de hoogte-breedteverhouding wilt behouden of de afmetingen wilt wijzigen in een opgegeven hoogte en breedte.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL According to]</td> 
   <td> <p>Selecteer hoe de module de nieuwe grootte van de afbeelding moet bepalen. Dit veld wordt weergegeven als u de verhouding tussen hoogte en breedte in het veld I wilt behouden. Andere velden worden weergegeven op basis van de selectie in dit veld.</p> 
    <ul> 
     <li> <p>[!UICONTROL Maximum width]</p> <p>Hiermee verkleint u een afbeelding tot een door u opgegeven breedte. De hoogte wordt automatisch berekend.</p> </li> 
     <li> <p>[!UICONTROL Maximum height]</p> <p>Hiermee verkleint u een afbeelding tot een door u opgegeven hoogte. De breedte wordt automatisch berekend.</p> </li> 
     <li> <p>[!UICONTROL Maximum height or width]</p> <p>Hiermee verkleint u een afbeelding zodanig dat de hoogte en breedte ervan de opgegeven waarden niet overschrijden. Omdat bij deze optie de hoogte-breedteverhouding behouden blijft, kan een van de afmetingen kleiner zijn dan opgegeven. Als hoogte en breedte bijvoorbeeld beide zijn opgegeven als 40, wordt een afbeelding van 400 x 300 verkleind tot 40 x 30.</p> </li> 
     <li> <p>[!UICONTROL Minimum width]</p> <p>Hiermee vergroot u een afbeelding tot een door u opgegeven breedte. De hoogte wordt automatisch berekend.</p> </li> 
     <li> <p>[!UICONTROL Minimum height]</p> <p>Hiermee vergroot u een afbeelding tot een door u opgegeven hoogte. De breedte wordt automatisch berekend.</p> </li> 
     <li> <p>[!UICONTROL Minimum height or width]</p> <p>Hiermee vergroot u een afbeelding zodanig dat de hoogte en breedte niet kleiner zijn dan de waarden die u opgeeft. Omdat bij deze optie de hoogte-breedteverhouding behouden blijft, kan een van de afmetingen groter zijn dan opgegeven. Als hoogte en breedte bijvoorbeeld beide zijn opgegeven als 300, wordt een afbeelding van 40 x 30 vergroot tot 400 x 300.</p> </li> 
     <li> <p>[!UICONTROL Percent]</p> <p>Hiermee wijzigt u de afbeeldingsgrootte met een percentage op basis van de waarde die u opgeeft. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Width]</td> 
   <td>Voer de gewenste breedte van de gewijzigde afbeelding in pixels in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Height]</td> 
   <td>Voer de gewenste hoogte van de gewijzigde afbeelding in pixels in of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Change by percentage]</td> 
   <td>Als u de afbeelding wilt wijzigen op basis van een percentage, voert u het percentage in of wijst u dit percentage toe waarmee u de afbeelding wilt wijzigen.</td> 
  </tr> 
 </tbody> 
</table>

## Problemen oplossen

### Handeling beëindigd met een fout

een handeling kan worden beëindigd met een fout vanwege een van de volgende oorzaken:

* De ontvangen gegevens hebben niet de JPG/GIF/PNG/BMP-indeling
* De maximale breedte/hoogte is overschreden bij het wijzigen van de afmetingen van de afbeelding. De afbeelding mag niet groter zijn dan 3840 px breedte en 2160 px hoogte
* De maximaal toegestane grootte van een afbeelding is overschreden tijdens het wijzigen van de afmetingen of de indeling van de afbeelding.
