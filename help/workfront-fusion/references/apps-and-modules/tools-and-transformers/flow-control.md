---
title: Stroomregeling
description: Wanneer u een scenario creeert of uitgeeft, kunt u montages vormen om de manier te controleren de gegevens door het stromen.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# Stroomregeling

Wanneer u een scenario creeert of uitgeeft, kunt u montages vormen om de manier te controleren de gegevens door het stromen.

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
   <p>Geen Workfront Fusion-licentievereiste</p>
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

## Repeater

Met een module [!UICONTROL Repeater] kunt u een taak een bepaald aantal keren herhalen. Een module [!UICONTROL Repeater] genereert bundels, een voor een.


<table>
    <tr>
        <td>[!UICONTROL Initial value]</td>
        <td>Ga of kaart de waarde in die u de module in de eerste herhaling wilt hebben. De standaardwaarde is 1.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Repeats]</td>
        <td>Ga of kaart het aantal tijden in dat u de module wilt herhalen. Dit getal moet groter dan of gelijk aan 0 zijn en kleiner dan of gelijk aan 10.000.</td>
    </tr>
    <tr>
        <td>[!UICONTROL Step]</td>
        <td>Dit is het aantal waardoor de module de waarde verhoogt. De standaardwaarde is 1.</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

Bijvoorbeeld, kon u een [!UICONTROL Repeater] module gebruiken om vijf e-mails met de onderwerpen &quot;Hello 1,&quot;Hello 2,&quot;te verzenden, etc., door de **[!UICONTROL Email]>[!UICONTROL Send me an email]** module aan de [!UICONTROL Repeater] module aan te sluiten.

1. Klik het [!UICONTROL Flow Control] pictogram van de de controlepictogram van de Stroom ![ ](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif) bij de bodem van het scherm, dan klik **[!UICONTROL Repeater]** in het menu dat toont.
1. Klik op de module [!UICONTROL Repeater] en klik vervolgens op **[!UICONTROL Connect automatically]** in het vak dat wordt weergegeven.

   De module Repeater wordt geopend.

1. Voer in het veld **[!UICONTROL Repeats]** het aantal herhalingen (uitvoerbundels) in dat de module moet produceren.

   In dit voorbeeld voert u 5 in.

   ![ Repeater ](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   De waarde van het item neemt in elke herhaling toe met de waarde die is opgegeven in het veld **[!UICONTROL Step]** . U kunt deze waarde weergeven door **[!UICONTROL Show advanced settings]** te selecteren. Dit getal is standaard 1.

1. Klik op **[!UICONTROL OK]** om het vak **[!UICONTROL Flow Control]** te sluiten.

1. Klik op de app of servicemodule die is verbonden met de module [!UICONTROL Repeater] .
1. Typ in het vak dat wordt weergegeven de informatie die u wilt herhalen.

   In ons e-mailvoorbeeld typt u Hello in het vak [!UICONTROL Subject] en wijst u vervolgens `i` toe vanuit de herhalingsmodule.

   ![ Repeater ](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>Het aantal herhalingen wordt niet bepaald door de waarde van `i`, zoals in een lus in programmering. In de module wordt het aantal keren herhaald dat wordt aangegeven in het veld [!UICONTROL Repeats] . De waarde `i` verandert bij elke herhaling van de module [!DNL repeater] en kan worden toegewezen aan latere modules. In het bovenstaande voorbeeld wordt de waarde van `i` toegewezen aan het Hello-bericht, wat resulteert in berichten die &quot;Hello 1,&quot; Hello 2,&quot; enzovoort lezen.

>[!ENDSHADEBOX]

## [!UICONTROL Iterator]

Een [!UICONTROL Iterator] is een speciaal type module dat een array omzet in een reeks bundels. Elk arrayitem wordt een afzonderlijke bundel in de uitvoer van de module [!UICONTROL Iterator] . Voor meer informatie, zie {de module van de Teller 0} ](/help/workfront-fusion/references/modules/iterator-module.md).[

## Arrayaggregator

Een arrayaggregator is een speciaal type module waarmee u verschillende bundels kunt samenvoegen tot één bundel. Voor meer informatie, zie [ de module van de Samenvoegaar ](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

De [!UICONTROL Router] module staat u toe om uw stroom in verscheidene routes te vertakken en de gegevens binnen elke route verschillend te verwerken. Zodra een [!UICONTROL Router] module een bundel ontvangt, door:sturen het aan elke verbonden route in de orde de routes aan de [!UICONTROL Router] module in bijlage waren. Voor meer informatie, zie [ module van de Router in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

## Richtlijnen

Met de instructies voor foutafhandeling kunt u bepalen hoe het scenario reageert op fouten.

Voor informatie over fout behandelende richtlijnen, zie [ Richtlijnen voor fout behandeling ](/help/workfront-fusion/references/errors/directives-for-error-handling.md).

