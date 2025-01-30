---
title: Stroomregeling
description: Wanneer u een scenario creeert of uitgeeft, kunt u montages vormen om de manier te controleren de gegevens door het stromen.
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---

# Stroomregeling

Wanneer u een scenario creeert of uitgeeft, kunt u montages vormen om de manier te controleren de gegevens door het stromen.

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan*</td>
  <td> <p>[!UICONTROL Pro] of hoger</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidige licentievereiste: geen [!DNL Workfront Fusion] licentievereiste.</p>
   <p>of</p>
   <p>Vereiste voor verouderde licentie: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en -integratie], [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] [!DNL Adobe Workfront] -abonnement hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] wordt opgenomen in het [!UICONTROL Ultimate] [!DNL Workfront] -abonnement.</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Repeater

Met een module [!UICONTROL Repeater] kunt u een taak een bepaald aantal keren herhalen. Een module [!UICONTROL Repeater] genereert bundels, een voor een.

Bijvoorbeeld, kon u een [!UICONTROL Repeater] module gebruiken om vijf e-mails met de onderwerpen &quot;Hello 1,&quot;Hello 2,&quot;te verzenden, etc., door de **[!UICONTROL Email]>[!UICONTROL Send me an email]** module aan de [!UICONTROL Repeater] module aan te sluiten.

Een module [!UICONTROL Repeater] gebruiken:

1. Klik het [!UICONTROL Flow Control] pictogram van de de controlepictogram van de Stroom ![ ](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif) bij de bodem van het scherm, dan klik **[!UICONTROL Repeater]** in het menu dat toont.
1. Klik op de bundel [!UICONTROL Repeater] en klik vervolgens op **[!UICONTROL Connect automatically]** in het vak dat wordt weergegeven.
1. Typ in het vak [!UICONTROL Flow Control] dat wordt weergegeven het gewenste aantal herhalingen (outputbundels) in het vak **[!UICONTROL Repeats]** .

   In ons e-mailvoorbeeld typt u 5.

   ![ Repeater ](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   De waarde van het item neemt in elke herhaling toe met de waarde die is opgegeven in het veld **[!UICONTROL Step]** . U kunt deze waarde weergeven door **[!UICONTROL Show advanced settings]** te selecteren. Dit getal is standaard 1.

1. Klik op **[!UICONTROL OK]** om het vak **[!UICONTROL Flow Control]** te sluiten.

1. Klik op de app of servicemodule die is verbonden met de module [!UICONTROL Repeater] .
1. Typ in het vak dat wordt weergegeven de informatie die u wilt herhalen.

   In ons e-mailvoorbeeld typt u Hello in het vak [!UICONTROL Subject] en wijst u vervolgens `i` toe vanuit de herhalingsmodule.

   ![ Repeater ](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)

| Item | Beschrijving |
|---|---|
| [!UICONTROL Initial value] | Voer in of wijs het nummer toe dat de module als `i` moet instellen in de eerste herhaling. De standaardwaarde is 1. |
| [!UICONTROL Repeats] | Ga of kaart het aantal tijden in dat u de module wilt herhalen. Dit getal moet groter dan of gelijk aan 0 zijn en kleiner dan of gelijk aan 10.000. |
| [!UICONTROL Step] | Dit is het getal waarmee de module de waarde van `i` verhoogt. De standaardwaarde is 1. |

{style="table-layout:auto"}

>[!NOTE]
>
>Het aantal herhalingen wordt niet bepaald door de waarde van `i`, zoals in een lus in programmering. In de module wordt het aantal keren herhaald dat wordt aangegeven in het veld [!UICONTROL Repeats] . De waarde `i` verandert bij elke herhaling van de module [!DNL repeater] en kan worden toegewezen aan latere modules. In het bovenstaande voorbeeld wordt de waarde van `i` toegewezen aan het Hello-bericht, wat resulteert in berichten die &quot;Hello 1,&quot; Hello 2,&quot; enzovoort lezen.

## [!UICONTROL Iterator]

Een [!UICONTROL Iterator] is een speciaal type module dat een array omzet in een reeks bundels. Elk arrayitem wordt een afzonderlijke bundel in de uitvoer van de module [!UICONTROL Iterator] . Voor meer informatie, zie {de module van de Teller 0} ](/help/workfront-fusion/references/modules/iterator-module.md).[

## Arrayaggregator

Een arrayaggregator is een speciaal type module waarmee u verschillende bundels kunt samenvoegen tot één bundel. Voor meer informatie, zie [ de module van de Samenvoegaar ](/help/workfront-fusion/references/modules/aggregator-module.md).

## [!UICONTROL Router]

De [!UICONTROL Router] module staat u toe om uw stroom in verscheidene routes te vertakken en de gegevens binnen elke route verschillend te verwerken. Zodra een [!UICONTROL Router] module een bundel ontvangt, door:sturen het aan elke verbonden route in de orde de routes aan de [!UICONTROL Router] module in bijlage waren. Voor meer informatie, zie [ module van de Router in  [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md).

<!--
<div>
<h2>Directives</h2>
<p>The error handling directives allow you to control how your scenario reacts to errors. For more information, see <a href="/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md" class="MCXref xref">Advanced error handling in Adobe Workfront Fusion</a> and <a href="/help/workfront-fusion/references/errors/directives-for-error-handling.md" class="MCXref xref">Directives for error handling in Adobe Workfront Fusion</a>.</p>
</div>
-->
