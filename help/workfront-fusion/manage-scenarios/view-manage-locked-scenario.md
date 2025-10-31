---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: Vergrendelde scenario's beheren
description: Vergrendelde scenario's beheren in Adobe Workfront Fusion
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Vergrendelde scenario&#39;s beheren

In sommige gevallen kan een scenario tijdelijk zijn vergrendeld in Workfront Fusion. Vergrendelde scenario&#39;s worden binnen 2-4 uur automatisch ontgrendeld. U kunt scenario&#39;s manueel ontgrendelen, maar het wordt over het algemeen niet geadviseerd.

Scenario&#39;s kunnen om een aantal redenen worden vergrendeld:

* Workfront Fusion ondersteunt geen parallelle verwerking van geplande scenario&#39;s. Deze scenario&#39;s worden gesloten aan het begin van de scenariouitvoering en ontgrendeld wanneer het voltooit. Als de uitvoering wordt onderbroken, kan het scenario niet ontgrendelen. Dit kan voorkomen wanneer een gebruiker manueel dwingen-houdt het scenario, of wanneer er een systeemkwestie is.

* Het technische team van Workfront Fusion kan een scenario vergrendelen omdat dit prestaties of andere problemen veroorzaakt.

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

## Een vergrendeld scenario ontgrendelen

Vergrendelde scenario&#39;s ontgrendelen 2 tot 4 uur vanaf het moment dat ze vergrendeld waren. U kunt een scenario manueel ontgrendelen alvorens het wordt gepland om automatisch te ontgrendelen.

>[!WARNING]
>
>Het ontgrendelen van een scenario kan fouten in de uitvoeringen van een scenario manueel veroorzaken. Wij adviseren manueel ontgrendelende scenario&#39;s slechts wanneer een scenario wegens het lopen en het tegenhouden van uitvoeringen als deel van het ontwerpen van het scenario wordt gesloten. In andere omstandigheden, adviseren wij dat u op het scenario wacht automatisch worden ontgrendeld.


Een vergrendeld scenario handmatig ontgrendelen:

1. Ga de de detailpagina van het Scenario van het gesloten scenario.
1. Klik op **[!UICONTROL Options]** in de rechterbovenhoek van het scherm.
1. Selecteer **[!UICONTROL Unlock execution]**.
1. Klik op **[!UICONTROL Unlock]**.
   ![ Ontgrendelingsscenario ](assets/unlock-scenario.png)
